pipeline {
    agent any
     tools { 
      maven 'LocalMaven' 
      jdk 'LocalJDK' 
      dockerTool 'docker1'	
    }
    stages {	        
	stage('Create Tomcat Docker Image'){
		
            steps {		
		echo "$USER"
		sh "whoami"
                sh "docker version"
            }
        }
    }
}
