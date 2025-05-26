pipeline {
    agent { label 'Joindevops-nodeJs' }
    stages {
        stage('Build') {
            steps {
               script{
                  sh """
                     echo 'Hello World this is build'
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
}