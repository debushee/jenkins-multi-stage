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
