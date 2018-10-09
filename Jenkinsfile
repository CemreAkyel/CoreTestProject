node {
  def app
  stage('start stage') {
    echo 'Hello World'
  }
    stage('Clone repository') {
        
        checkout scm
		echo 'ending of checkout!!!!....'
    }

   stage('docker hub stage'){
   /* image = docker.image('cnakyel/testrepo:firsttry')
    image.pull() */
	
	image=docker.image('hello-world')
	
	echo 	"ending"
   }
}
