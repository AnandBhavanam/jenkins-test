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

			steps {
				echo 'test2'
			}
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

		stage('Deploy- prod') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
