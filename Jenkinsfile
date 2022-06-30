pipeline {
	//agent any
	//agent { docker { image 'maven:3.6.3'} }
	agent { docker { image 'node:13.8'} }
	stages {
		stage('build') {
			steps {
				bash 'node --version'
				echo "build"
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
