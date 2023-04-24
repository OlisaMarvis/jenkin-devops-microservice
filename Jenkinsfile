//Declarative
pipeline {
  // agent any
  agent {
    docker {
    //   image 'maven:3.6.3'
	  image 'node:20-alpine3.16'
    }
  }
  stages {
    stage('Build') {
      steps {
        // sh 'mvn --version'
		sh 'node --version'
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
  }
  post {
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