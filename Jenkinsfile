pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                        cat mypassword.txt | sudo -S apt update
                        cat mypassword.txt | sudo apt install docker.io -y
                        docker build -t dockertest:latest .
                        docker images
                        docker run -d  -p 80:80 dockertest
                        docker ps
                        cp ${WORKSPACE}/index.html /var/www/html
                       """
                       
                }
            }
        }
    }
}
