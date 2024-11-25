pipeline {
     agent any
   stages {
     stage('Checkout') {
         steps {
              checkout scm
            }
        }
}
stage('Run Hello ') {
            steps {
                script {
                    
                    sh 'python3 hello.py'
                }
            }
        }
post {
         success {
              echo 'Build  successfully .'
           }
         failure {
              echo ' Build failed '
             }
         }
    }
