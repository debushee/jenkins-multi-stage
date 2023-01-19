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
                sh '''#!/bin/bash
                source venv/bin/activate
                sleep time: 10, unit: 'MINUTES'
                BUILD_ID=nokill gunicorn --bind=0.0.0.0:8001 hangman:app -D'''
            }
        }
        stage('Test') {
            steps {
                sh 'curl localhost:8001'
            }
        }
        stage('Clean Workspace') {
            steps {
                sh 'pkill gunicorn'
                cleanWs()
            }
        }
    }
}
