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
                       sudo -r cp index.html /var/www/html
                       """
                }
            }
        }
    }
}
