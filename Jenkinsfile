pipeline {
    agent any
    
    stages {
        stage('check version') {
            steps {
                sh './mvnw --version'
            }
        }
        stage('build') { 
            steps {
                sh './mvnw clean package'
            }
        }
    }
}
