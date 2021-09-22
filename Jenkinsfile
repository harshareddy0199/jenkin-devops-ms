pipeline {
	agent any
	//agent { docker { image 'maven 3.6.3' } }
	environment {
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'MyMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
	    stage('Checkout') {
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
		 stage('Build') {
			 steps {
				 sh "mvn clean compile"
            }
		 } 
	    stage('TEST') {
		    steps{
				sh "mvn test"
	        }
		}
		stage('QA') {
		    steps{
				sh "mvn failsafe:integration-test failsafe:verify"
	        }
	    }	
	} 
}
