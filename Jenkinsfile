pipeline {
	agent any
	//agent { docker { image 'maven 3.6.3' } }
	environment {
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'MyMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
	    stage('Build') {
		    steps {
				echo "Build"
				echo "$path"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
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
