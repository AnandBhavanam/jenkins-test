pipeline {
	agent any

	stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('push data') {
			when {
				
                    branch 'main'
			
			}

			steps {
                echo 'deploy Deploying....'
            }
        }

		stage('Deploy- prod') {
            steps {
                echo 'Deploying....'
            }
        }
    }
	post {
		always {
			echo 'i'm awesome
		}

		success {
			echo 'i run when ur successful'
		}

		failure {
			echo 'i runs when ur failed'
		}

		changes {
			echo 'i run when the status is changed'
		}
	}
}
