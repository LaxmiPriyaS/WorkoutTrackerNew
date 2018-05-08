pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                bat 'scripts/test.sh'
            }
        }
        stage('Deliver') {
            steps {
                bat '/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                
            }
        }
    }
}
s
