pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/Lingaraj-1/ci-cd-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8082:80 cicd-app || true'
            }
        }
    }
}

