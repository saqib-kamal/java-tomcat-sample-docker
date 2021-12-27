pipeline {
    agent any
     tools { 
      maven 'LocalMaven' 
      jdk 'LocalJDK' 
      dockerTool 'myDocker'	
    }
    stages {
	
        stage('Build Application') {
            steps {
		echo "Building project"				
                sh "mvn -f pom.xml clean package"
		echo "finished building project"
            }
            post {
                success {
                    echo "Now Archiving the Artifacts...."
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
	stage('Create Tomcat Docker Image'){
		
            steps {		
		echo "Build docker image"
                sh "docker build . -t tomcatsamplewebapp:${env.BUILD_ID}"
            }
        }
    }
}
