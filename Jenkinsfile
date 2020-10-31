pipeline {
	//agent { docker { image 'maven:3.6.3'} }
	agent any

	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
        stage('Build') {
            steps {
                echo "mvn --version"
				echo "$PATH"
				echo "build tag- $env.BUILD_TAG"
				echo "build version- $env.BUILD_URL"
				echo "Build Number - $env.BUILD_NUMBER"
				echo "build tag- $env.JOB_NAME"
				echo "build tag- $env.BUILD_ID"
				//sh "mvn clean install"
            }
        }
		stage('Package') {
			steps {
				sh 'mvn package -DskipTests'
			}
		}

		stage('Docker Build') {
			steps {
				script {
					dockerImage = docker.build("anand47r/exchange:0.0.1")
				}
			}
		}

		stage('Docker push') {
			steps {
				script {
					docker.withRegistry('','dockerhub') {
						dockerImage.push();
                    	dockerImage.push('latest');
					}
				}
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
