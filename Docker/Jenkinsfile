pipeline {
    agent { 
        docker { image 'python:latest' } 
        }
    stages {
        stage('Build Docker image') {
            steps {
                sh """
                  cd Docker
                  pwd
                  ls -la
                   """
            }
        }
    }
}
