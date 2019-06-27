pipeline{
    agent any
    environment {
        CI = 'true'
    }
    stages('Build') {
        stage('Build') {
            steps {
                sh 'npm -v'
                sh 'npm install'
                sh 'node -v'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}