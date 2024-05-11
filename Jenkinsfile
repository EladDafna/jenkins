pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            steps {
                script {
                    docker.image('docker:19.03.12').inside('-v /var/run/docker.sock:/var/run/docker.sock') {
                        sh 'docker build -t mydockerimage:latest .'
                        sh 'docker images'
                    }
                }
            }
        }
    }
}
