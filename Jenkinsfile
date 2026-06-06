pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t gangadharbv/cicd-k8s:v1 .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push gangadharbv/cicd-k8s:v1'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl rollout restart deployment/cicd-app'
            }
        }
    }
}
