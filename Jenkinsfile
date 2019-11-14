pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5001:5001' 
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build1') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test1') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}