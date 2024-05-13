pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                    
                        apt update
                        apt install sudo
                        sudo apt install docker.io
                        docker build -t dockertest:latest .
                        docker images
                       """
                       
                }
            }
        }
    }
}
