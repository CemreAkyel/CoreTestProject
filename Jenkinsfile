pipeline {
    agent any
    stages {
		stage('Start') {
            steps {
                echo 'starting from git..'
            }
        }
		stage('Checkout') {
            steps {
				checkout scm
            }
        } 
		stage('Building') {
			steps {
				app = docker.build("coretestproject")
			
                echo 'Building from git..'
				}
		}
    }
}

