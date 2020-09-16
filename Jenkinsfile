pipeline {
	agent any
	stages {
		stage('Clean workspace') {
			steps {
				deleteDir()
			}
		}
		stage('Checkout SCM') {
			steps {
				echo 'hey SCM'
			}
		}
		stage('Build') {
			steps {
				echo 'building now'
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}
