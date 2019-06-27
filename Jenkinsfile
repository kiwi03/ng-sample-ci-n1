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
       /*  stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        } */
        stage('Deliver') { 
            steps {
                sh './jenkins/scripts/deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                // sh './jenkins/scripts/kill.sh' 
            }
        }
    }
}