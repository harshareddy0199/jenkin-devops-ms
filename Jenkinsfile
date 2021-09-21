pipeline {
	agent { docker { image 'maven 3.6.3' } }
	stages {
	    stage('Build') {
		    steps{
				sh 'mvn --version'
				echo "Build"
	        }
		}	
	    stage('TEST') {
		    steps{
				echo "TEST"
	        }
		}
		stage('QA') {
		    steps{
				echo "INTEGRATION TEST"
	        }
	    }	
	}
}
