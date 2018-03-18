pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                shell 'mvn -B -DskipTests clean package' 
            }
        }
    }
}