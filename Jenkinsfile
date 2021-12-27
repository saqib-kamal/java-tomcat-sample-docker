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
                sh 'mvn --version'
		echo "finished building projj"
            }    
        }		
    }
}
