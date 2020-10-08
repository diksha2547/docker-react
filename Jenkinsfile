#!groovy

import groovy.json.JsonOutput

def gitInfo='Diksha'

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
				script {
                    dockerImageTag = "${env.BRANCH_NAME}-${gitInfo.git_commit}"
				}
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