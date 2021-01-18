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
        stage('pwd') { 
            steps {
                sh 'cat ~/.ssh/id_rsa.pub' 
            }
        }
}
}
