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
				not {
                    branch 'main'
				}
			}
        }

		stage('Deploy- prod') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
