pipeline {
    agent any
    stages {
        stage('Repo') {
            steps {
                git 'https://github.com/Crush-Steelpunch/hangman'
            }
        }
        stage('Dependencies') {
            steps {
                sh '''#!/bin/bash
                python3 -m venv venv
                source venv/bin/activate
                pip3 install -r requirements.txt''' 
            }
        }
        stage('Build') {
            steps {
                sh '''
                #!/bin/bash
                gunicorn --bind=0.0.0.0:8001 hangman:app -D'''
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
