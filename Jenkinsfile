def gitInfo='Diksha'


node {

	
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