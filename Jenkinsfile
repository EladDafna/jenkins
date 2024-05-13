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
                        docker run -d --name apache_test -p 80:80 dockertest
                        docker ps
                        docker cp index.html apache_test:/var/www/html/
                       """
                       
                }
            }
        }
    }
}
