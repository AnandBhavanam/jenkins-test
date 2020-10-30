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
			echo 'im awesome'
		}
		success {
			echo 'i run when ur successful'
		}
		failure {
			echo 'i runs when ur failed'
		}
		changed {
			echo 'i run when the status is changed'
		}
	}
}
