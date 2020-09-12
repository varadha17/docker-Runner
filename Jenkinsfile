pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage('Docker Up') {
            steps {
                //sh
                bat "docker-compose up"
            }
        }
        stage('Docker Down') {
            steps {
                //sh
                bat "docker-compose down"
			}
        }	
	}
}	