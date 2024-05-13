pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                        docker cp index.html admiring_bardeen:/var/www/html/
                       """
                       
                }
            }
        }
    }
}
