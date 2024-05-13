pipeline {
    agent any
    stages {
        stage ('Build Docker image') {
            steps {
                script {
                 sh 'exec -it jenkins_container -u=root bash'
                }
            }
        }
    }
}
