pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            steps {
                sh """
                  cd Docker
                  docker build -t mydockerimage:latest .
                  docker images
                   """
            }
        }
    }
}
