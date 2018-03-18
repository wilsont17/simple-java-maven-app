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
				sh 'gradle wrapper' 
                sh 'gradle build' 
            }
        }
		stage('Test') {
            steps {
                sh './gradlew tasks'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}