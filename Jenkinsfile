pipeline {
    agent {
        docker {
            image 'gradle:3-alpine' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'gradle -B -DskipTests clean package'
            }
        }
    }
}