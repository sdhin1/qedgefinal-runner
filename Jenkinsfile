pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh for mac
                bat "docker-compose up --no-colors"
            }
        }
        stage('Bring Grid down') {
            steps {
                //sh for mac
                bat "docker-compose down"
            }
        }
    }
}