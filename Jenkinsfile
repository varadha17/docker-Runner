pipeline {
    // master executor should be set to 0
    agent any
    stages {
		stage('Pull Latest Image') {
			steps {
				bat "docker pull varadharajan17/selenium-test"
			}
		}
        stage('Docker Up') {
            steps {
                //sh
                bat "docker-compose up -d hub chrome firefox"
            }
        }
		stage('Run Test') {
            steps {
                //sh
                bat "docker-compose up seleniumtest"
            }
        }
	}
    post {
        always {
            archiveArtifacts artifacts: "output/**"
            bat "docker-compose down"
		}
    }	
}	