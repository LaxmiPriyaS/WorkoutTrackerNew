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
                bat 'test.sh'
            }
        }
        stage('Deliver') {
            steps {
                bat 'deliver.sh'
            }
        }
    }
}

