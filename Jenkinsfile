node {
  def app
  stage('HelloWorld') {
    echo 'Hello World'
  }
    stage('Clone repository') {
        
        checkout scm
		echo 'ending of checkout!!!!....'
    }

   stage('Image from docker hub') {
    image = docker.image('cnakyel/testrepo:firsttry')
    image.pull() 
	echo 	'ending .....'
   }
}
