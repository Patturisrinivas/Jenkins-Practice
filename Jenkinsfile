pipeline {
    agent { label 'Joindevops-nodeJs' }
    environment {
        project = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    options{
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'SECONDS')
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
                   sleep 30
                 """
               }
            }
        }
        stage('Deploy'){
            steps {
               script{
                sh """
                  echo 'hello world this is deployment'
                  sleep 45
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