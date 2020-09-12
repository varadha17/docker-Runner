pipeline {
    // master executor should be set to 0
    agent any
    stages {
        stage("Docker Up") {
            steps {
                //sh
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage("Run Test") {
            steps {
                //sh
                bat "docker-compose up seleniumtest"
            }
        }
		stage("Docker Down") {
			steps {
				bat "docker-compose down"
		}
	}
}	