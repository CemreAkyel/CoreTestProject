node {
  def image
  stage('start stage') {
	echo 'Hello World'
  }
    stage('Check repository') {        
        checkout scm
		echo 'ending of checkout!!!!....'
    }

   stage('Pull From Docker Hub'){
   /* image = docker.image('cnakyel/testrepo:firsttry')
    image.pull()*/
	
	docker-compose -f docker-compose.yml build
    docker-compose -f docker-compose.yml -p dockerComposeProjectTest up    --abort-on-container-exit
	
	echo 	"Image pulled from docker hub successfully..."
   }
   
   stage('Run Image'){
	/*myContainer = image.run('--name  test-from-dockerhub-container -p 8080:37700') */
	echo 	"Run image"
   }
   
}
