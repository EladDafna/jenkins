pipeline {
    agent {
        docker
    }
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
