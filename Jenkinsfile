pipeline {
   agent any
   stages {
      stage('Build'){
         steps {
            echo "building..."
            sh 'mvn clean package'
         }
      }
      stage('Deploy to stage'){
         steps {
            echo "deploying to stage..."
            build job: 'deploy-to-staging'
         }
         post {
            success {
               echo "Now archiving..."
               archiveArtifacts artifacts: '**/target/*.war'
            }
         }
      }
      stage('Deploy to Production'){
         steps {
            echo "Deploying to production..."
         }
      }
   }
}
