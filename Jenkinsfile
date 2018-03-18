pipeline {
    agent {
        docker {
            image 'gradle:alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
				sh 'git update-index --chmod=+x gradlew'
                sh './gradlew build' 
            }
        }

    }
}