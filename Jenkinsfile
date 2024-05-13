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
                        docker run -d --name apache_test -p 80:80 dockertest:latest
                        docker ps
                        docker cp index.html apache_test:/var/www/html/
                        docker tag  dockertest:latest eladdafna/dockertest:latest
                        docker push eladdafna/dockertest:latest
                        docker images
                       """
                       
                }
            }
        }
    }
}
