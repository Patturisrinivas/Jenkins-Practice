pipeline {
    agent { label 'Joindevops-nodeJs' }
    environment {
        project = 'EXPENSE'
        COMPONENT = 'BACKEND'
    }
    options{
        disableConcurrentBuilds()
        timeout(time: 5, unit: 'MINUTES')
    }
    Parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
               script{
                  sh """
                     echo 'Hello World this is build'
                     echo "Project: $PROJECT"
                     echo "Hello ${params.PERSON}"
                     echo "Biography: ${params.BIOGRAPHY}"
                     echo "Toggle: ${params.TOGGLE}"
                     echo "Choice: ${params.CHOICE}"
                     echo "Password: ${params.PASSWORD}"
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