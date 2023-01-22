pipeline {
    agent any
  
    //create dockerhub credential in github with your dockerhub Username and Password/Token
    environment {
      DOCKERHUB_CREDENTIALS=credentials('dockerhub')
    }
    
    stages {
      
        stage('Checkout') {
            steps {
                git url: 'https://github.com/adeoyedewale/BackendFrontend.git'
            }
        }
      
        stage('Build Backend') {
            steps {
                sh 'cd backend && npm install'
                sh 'cd ..'
            }
        }
        stage('Build Frontend') {
            steps {
                sh 'cd frontend && npm install'
                sh 'cd ..'
            }
        }
        stage('Build Images') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('Push Images to Registry') {
            steps {
                sh 'docker-compose push'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
