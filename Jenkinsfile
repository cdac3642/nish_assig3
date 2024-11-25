pipeline {
     agent any
   environment {
         DOCKER_IMAGE = 'hello-python:latest' //dokcer image name
 }
   stages {
     stage('Checkout') {
         steps {
              checkout scm
            }
        }
   stage('Run Hello ') {
            steps {
                script {
                    
                    sh 'python3 hello.py'
                }
            }
        }
   stage('Build') {
       steps {
            sh """
            docker build -t $DOCKER_IMAGE .
              """
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
