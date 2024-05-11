pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            steps {
                sh """
                  docker build -t mydockerimage:latest .
                  docker images
                   """
            }
        }
    }
}
