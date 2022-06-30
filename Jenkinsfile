pipeline {
	agent any
	stages {
		stage('build') {
			steps {
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

	} post {
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
