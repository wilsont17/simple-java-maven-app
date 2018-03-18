pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                shell 'gradle build -x test' 
            }
        }
    }
}