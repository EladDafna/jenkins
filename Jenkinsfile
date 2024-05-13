pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                    
                        cat mypassword.txt | sudo -S apt update
                        docker build -t dockertest:latest .
                        docker images
                       """
                       
                }
            }
        }
    }
}
