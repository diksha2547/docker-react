pipeline {
	agent any
	environment {
    		registry = "dikshagupta04"
    		registryCredential = 'Skidv@70449'
    		dockerImage = ''
  	}
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
				script {
					dockerImage = docker.build registry + ":$BUILD_NUMBER"
				}
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}