pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                script {
                    sh """
                       echo "Hello, this is build"
                    """
                }
              
            }
        }
        stage ('Test') {
            steps {
                scrip{
                    sh """
                       echo "Hello, this is test"
                    """
                }
        
            }
        stage ('deploy') {
            steps {
                scrip{
                    sh """
                       echo "Hello, this is deploy"
                    """
                }
        
            }
       }
    }

}