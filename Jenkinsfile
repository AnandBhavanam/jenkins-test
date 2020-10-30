pipeline {
	agent any

	stages {

	
		stage('Compile stage') {
			withMaven(maven : 'myMaven') {
				sh 'mvn clean install'
			}
		}
		stage('Test') {
			echo "Test"
	 	}
	}
}
