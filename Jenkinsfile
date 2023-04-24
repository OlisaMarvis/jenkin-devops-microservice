//SCRIPTED
// node {
// 	echo "Build"
// 	echo "Test"
// 	echo "Test Integration Test"
// }

//Declarative
pipeline {
	agent {docker {image 'maven:3.6.3'} }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} post {
		always {
			echo 'I am awesom, I run always'
		}
		success {
			echo 'I run when you are succesful'
		}
		failure {
			echo 'I run when you fail'
		}
	}
	
}