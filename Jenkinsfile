pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                    
                        cat mypassword.txt | sudo -S apt update
                        cat mypassword.txt | sudo apt install docker.io
                        docker build -t dockertest:latest .
                        docker images
                       """
                       
                }
            }
        }
    }
}
