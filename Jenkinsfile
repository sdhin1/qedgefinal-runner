pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Start Grid') {
            steps {
                //sh for mac
				bat "docker system prune -f"
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage('Run Test') {
            steps {
                //sh for mac
                bat "docker-compose up QEdge_xml"
            }
        }
        stage('Stop Grid') {
            steps {
                //sh for mac
                bat "docker-compose down"
            }
        }
    }
}