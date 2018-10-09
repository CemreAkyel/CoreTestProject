node {
  def app
  stage('HelloWorld') {
    echo 'Hello World'
  }
    stage('Clone repository') {
        
        checkout scm
		echo 'ending of checkout!!!!....'
    }

   stage{
   /* image = docker.image('cnakyel/testrepo:firsttry')
    image.pull() */
	
	docker run hello-world
	echo 	"ending"
   }
}
