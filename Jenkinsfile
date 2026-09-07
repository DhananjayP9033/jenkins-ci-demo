pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
                sh 'ls -la'
            }
        }

        stage('Setup') {
            steps {
                echo 'Creating Python virtual environment...'
                sh 'python3 -m venv .venv'
                sh '.venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh '.venv/bin/python -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '.venv/bin/pytest -q'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
