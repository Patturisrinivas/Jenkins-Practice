pipeline {
    agent { label 'Joindevops-nodeJs' }
    environment {
        project = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    options{
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
               script{
                  sh """
                     echo 'Hello World this is build'
                     echo "Project: $PROJECT"
                     sleep 15
                   """
                }
            }
        }
        stage('Test') {
            steps {
               script{
                sh """
                   echo 'hello world this test'
                 """
               }
            }
        }
        stage('Deploy'){
            steps {
               script{
                sh """
                  echo 'hello world this is deployment'
                """
               } 
            }
        }
    }
    post {
        always{
            echo 'i will always say Hello again!'
        }
        failure {
            echo 'i will run when pipeline is failed'
        }
        success{
            echo 'i will run when pipeline is success'
        }
    }
}