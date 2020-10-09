#!groovy

import groovy.json.JsonOutput

def gitInfo='Diksha'


pipeline {
	def app
	options {
        buildDiscarder(logRotator(numToKeepStr:'5'))
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
				script {
                    dockerImageTag = "${env.BUILD_NUMBER}"
					echo "the change owner ${gitInfo} - ${dockerImageTag}"
				}
			}
		}
		stage('Build') {
			steps {
				app = docker.build(diksha2547/docker-react)
				
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}