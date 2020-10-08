pipeline {
	options {
        buildDiscarder(logRotator(numToKeepStr:'10'))
        timestamps()
    }
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
				echo 'building'
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}