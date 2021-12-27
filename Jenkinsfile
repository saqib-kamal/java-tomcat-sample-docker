pipeline {
    agent any
    tools { 
      maven '3.8.1' 
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
