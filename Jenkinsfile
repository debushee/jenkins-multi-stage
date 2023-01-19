pipeline {
    agent any
    stages {
        
        stage('Dependencies') {
            steps {
                sh 'python3 -m venv venv'

                sh 'pip3 install -r requirements.txt'
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
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
    }
}
