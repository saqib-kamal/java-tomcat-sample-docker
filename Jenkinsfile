pipeline {
    agent any
    stages {
        stage('Build Application') {
            steps {
		echo "Building project"		
                sh "/usr/share/maven/bin -f pom.xml clean package"
		echo "finished building projj"
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
