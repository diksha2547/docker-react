def gitInfo='Diksha'


node {

	
		stage('Clean workspace') {
			
				deleteDir()
			
		}
		stage('Clone sources') {
			echo 'hey'
		}
		stage('Build') {
			
				app = docker.build("diksha2547/docker-react")
				
			
		}
		stage('test') {
			
				echo 'testing'
			
		}
	
}