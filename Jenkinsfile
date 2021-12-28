pipeline {
    agent any
     tools { 
      
      dockerTool 'myDocker'	
    }
    stages {	        
	stage('Create Tomcat Docker Image'){
		
            steps {		
		sh "grep docker /etc/group"
		sh "whoami"
		sh "whereis docker"
                sh "docker version"
            }
        }
    }
}
