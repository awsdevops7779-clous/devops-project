pipeline {
    agent any
stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/awsdevops7779-clous/devops-project.git'
            }
        }
stage('Build Docker Image') {
            steps {
                sh 'docker build -t awsdevopsdev/devops-app:latest .'
            }
        }
stage('Push Docker Image') {
            steps {
                sh 'docker push awsdevopsdev/devops-app:latest'
            }
        }
stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}
