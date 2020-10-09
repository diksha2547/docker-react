#!groovy

import groovy.json.JsonOutput

def gitInfo='Diksha'


pipeline {
	options {
        buildDiscarder(logRotator(numToKeepStr:'5'))
        timestamps()
    }
	agent {
		dockerfile true
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
				script {
                    dockerImageTag = "${env.BUILD_NUMBER}"
					echo "the change owner ${gitInfo} - ${dockerImageTag}"
				}
			}
		}
		stage('Build') {
			steps {
				echo 'build'
				
			}
		}
		stage('test') {
			steps {
				echo 'testing'
			}
		}
	}
}