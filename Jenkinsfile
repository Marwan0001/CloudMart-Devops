pipeline {
    agent {
        label 'docker'
    }

    stages {
        stage('Build Backend Image') {
            steps {
                script {
                    sh 'docker build -t marwanmw/cloudmart-backend:latest -f backend/Dockerfile .'
                }
            }
        }

        stage('Build Frontend Image') {
            steps {
                script {
                    sh 'docker build -t marwanmw/cloudmart-frontend:latest -f frontend/Dockerfile .'
                }
            }
        }
        stage('Push Backend Image') {
            steps {
                script {
                    sh 'docker push marwanmw/cloudmart-backend:latest'
                }
            }
        }
        stage('Push Frontend Image') {
            steps {
                script {
                    sh 'docker push marwanmw/cloudmart-frontend:latest'
                }
            }
        }

    }
}