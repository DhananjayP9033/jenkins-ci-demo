pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
                sh 'ls -la'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'python3 -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
} 
