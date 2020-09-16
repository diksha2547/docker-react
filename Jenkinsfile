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
			agent any
			steps {
				sh 'docker build -t dg04/docker-react -f Dockerfile.dev .'
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}
