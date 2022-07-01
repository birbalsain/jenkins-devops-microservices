pipeline {
	agent any
	//agent { docker { image 'maven:3.6.3'} }
	// agent { docker { image 'node:13.8'} }
	environment {
		dockerHome = tool 'Mymaven'
		mavenHome = tool 'Mydocker'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('build') {
			steps {
				echo "build"
				echo "path - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "job name  - $env.JOB_NAME"
				echo "BUILD tag - $env.BUILD_TAG"
				echo "build url - $env.BUILD_URL"
			}
		}
		stage('Test') {
			steps {
				echo "test"
			}
		}
		stage('integration stage') {
			steps {
				echo "integration test"
			}
		}

	} 
	post {
		always {
			echo " i am runnin galways"
		}
		success {
			echo " i am running when buils success"
		}
		failure {
			echo " i run when build failed"
		}
	}
}
