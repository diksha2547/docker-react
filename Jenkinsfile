pipeline {
	agent any
	stages {
		stage('Clean workspace') {
			steps {
				deleteDir()
			}
		}
		stage('Clone sources') {
			steps {
				git url: 'https://github.com/diksha2547/docker-react.git'
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
