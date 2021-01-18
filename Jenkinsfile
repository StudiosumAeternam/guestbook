pipeline {
    agent any
    
    stages {
        stage('check version') {
            steps {
                sh 'mvn --version'
            }
        }
        stage('build') { 
            steps {
                sh './mvnw clean package'
            }
        }
    }
}
