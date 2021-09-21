pipeline {
	agent { 
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
