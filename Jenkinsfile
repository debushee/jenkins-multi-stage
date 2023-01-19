pipeline {
    agent any
    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Dependencies') {
            steps {
                sh '''python3 -m venv venv
                source venv/bin/activate
                pip3 install -r requirements.txt'''
            }
        }
        stage('Build') {
            steps {
                echo 'Hi'
            }
        }
        stage('Test') {
            steps {
                echo 'Hi'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hi'
            }
        }
    }
}
