node {
  def app
  stage('HelloWorld') {
    echo 'Hello World'
  }
    stage('Clone repository') {
        
        checkout scm
		echo 'ending of checkout!!!!....'
    }

    stage('Build image') {
        /* This builds the actual image; synonymous to
         * docker build on the command line */
        app = docker.build("coretestproject")
    }
}
