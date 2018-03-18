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
				sh 'chmod 755 ./gradlew'
                sh './gradlew build' 
            }
        }
		stage('Test') {
            steps {
                sh './gradlew test'
            }
			post {
                always {
                    junit 'build/test-results/test/*.xml' 
                }
            }
        }
		stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }
    }
}