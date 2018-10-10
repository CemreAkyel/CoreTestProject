node {
  def image
  stage('Start stage') {
	echo 'Hello World'
  }
   stage('DockerCompose Build Stage'){  
		sh 'docker-compose -f docker-compose.yml build'		
		echo 	"docker-compose build completed successfully..."
   }    
	stage('DockerCompose Up Stage'){
		sh 'docker-compose -f docker-compose.yml -p dockerComposeProjectTest up -d' 
		/*--abort-on-container-exit*/	
		echo 	"docker-compose up completed successfully..."
	}
}