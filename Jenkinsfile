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
         }
      }
      stage('Deploy to Production'){
         steps {
            echo "Deploying to production..."
         }
      }
   }
}
