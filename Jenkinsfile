pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'gradle -B -DskipTests clean package'
            }
        }
    }
}