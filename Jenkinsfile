pipeline{
    agent any
    stages('Build') {
        stage('Build') {
            steps {
                sh 'npm -v'
                sh 'npm install'
                sh 'node -v'
            }
        }
    }
}