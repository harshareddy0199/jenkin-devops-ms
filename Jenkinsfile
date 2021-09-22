pipeline {
	agent any
	//agent { docker { image 'maven 3.6.3' } }
	stages {
	    stage('Build') {
		    steps{
				//sh 'node --version'
				echo "Build"
				echo "$path"
				echo "BUILD_NUMBER - env.BUILD_NUMBER"
				echo "CBUILD_ID"
				echo "JOB_NAME - env.JOB_NAME"
				echo "BUILD_TAG - env.BUILD_TAG"
				echo "BUILD_URL"
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
