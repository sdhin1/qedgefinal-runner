pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Run Test') {
            steps {
                //sh for mac
				bat "docker system prune -f"
                bat "docker-compose up"
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