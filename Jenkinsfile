pipeline {
    agent {
        docker {
            image 'gradle:alpine' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                bat 'gradle -B -DskipTests clean package' 
            }
        }
		
    }
}