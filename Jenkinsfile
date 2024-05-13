pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                        sh 'docker build -t dockertest:latest .'
                        sh 'docker images'
                }
            }
        }
    }
}
