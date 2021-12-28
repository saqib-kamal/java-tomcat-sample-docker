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
		sh "pwd"
		sh "whoami"
		sh "whereis docker"
                sh "docker version"
            }
        }
    }
}
