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
        stage ('Deploy index.html to Apache') {
            steps {
                script {
                    sh """
                       pwd
                       ls -la
                       apt update
                       apt install sudo
                       sudo cp index.html /var/www/html
                       """
                }
            }
        }
    }
}
