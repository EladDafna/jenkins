pipeline {
    agent any
    environment {
        DOCKERHUB_USER = credentials('DOCKERHUB_USER')
        DOCKERHUB_PASSWORD = credentials('DOCKERHUB_PASSWORD')
   }
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                    sh """
                        cat mypassword.txt | sudo -S apt update
                        cat mypassword.txt | sudo apt install docker.io -y
                          docker build -t dockertest:latest .
                        docker run -d --name apache_test -p 80:80 dockertest:latest
                        docker ps
                        docker cp index.html apache_test:/var/www/html/
                        docker login -u ${DOCKERHUB_USER} -p ${DOCKERHUB_PASSWORD}
                        docker tag  dockertest:latest eladdafna/dockertest:latest
                        docker push eladdafna/dockertest:latest
                        docker images
                       """
                       
                }
            }
        }
    }
}
