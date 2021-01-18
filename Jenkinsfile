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
        stage('push to dev') { 
            steps {
                sh 'rsync -avzhe "ssh -p5022" ./targed/*.jar centos@$(cat /root/dev_ip)/var/project/app/artifact.jar' 
            }
        }
}
}
