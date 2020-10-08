#!groovy

import groovy.json.JsonOutput

def gitInfo

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
				checkout scm
				script {
					gitInfo = getGitInfo()
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