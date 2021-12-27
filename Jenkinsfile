pipeline {
    agent any
     tools { 
      maven 'LocalMaven' 
      jdk 'LocalJDK' 

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
                sh "docker build . -t tomcatsamplewebapp:${env.BUILD_ID}"
            }
        }
    }
}
