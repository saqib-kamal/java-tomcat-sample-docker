pipeline {
    agent any
     tools { 
      maven 'LocalMaven' 
      jdk 'LocalJDK' 
      dockerTool 'myDocker'	
    }
    stages {	        
	stage('Create Tomcat Docker Image'){
		
            steps {		
		echo "Build docker image"
                sh "docker version"
            }
        }
    }
}
