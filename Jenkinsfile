pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                        cp ${WORKSPACE}/index.html /var/www/html
                       """
                       
                }
            }
        }
    }
}
