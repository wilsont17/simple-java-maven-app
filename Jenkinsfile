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
                sh 'gradle build' 
            }
        }
		stage('Test') {
            steps {
                sh 'gradle test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}