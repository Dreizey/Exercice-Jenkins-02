pipeline {
    agent any

    stages {

        stage('Build Maven') {
            steps {
                sh './mvnw clean package'
            }
        }

        stage('Docker Build & Run') {
            steps {
                sh 'docker compose up -d --build'
            }
        }

    }
}