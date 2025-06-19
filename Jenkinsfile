pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Blackmoon390/kimai-docker.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t kimai-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
