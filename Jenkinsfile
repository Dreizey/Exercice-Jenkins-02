pipeline {
    agent any

    stages {
        stage('Build Maven') {
            steps {
<<<<<<< HEAD
                sh 'mvn clean package'
=======
                sh './mvnw clean package'
>>>>>>> parent of c3eafbc (Modif JenkinsFile)
            }
        }

        stage('Docker Build & Run') {
            steps {
                sh 'docker compose up -d --build'
            }
        }
    }
}