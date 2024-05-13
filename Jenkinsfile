pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                        sudo apt update
                        sudo apt install docker.io
                        docker build -t dockertest:latest .
                        docker images
                       """
                       
                }
            }
        }
    }
}
