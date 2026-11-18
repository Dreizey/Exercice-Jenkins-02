pipeline {
    agent any

    stages {
        stage('Maven Package') {
            agent {
                docker {
                    image 'maven:3.10.0-eclipse-temurin-21'
                    args '''
                        -v $HOME/.m2:/root/.m2:z
                        -u root
                    '''
                    reuseNode true
                }
            }
            steps {
                sh 'mvnw clean package'
            }
        }

        stage('Docker Build & Run') {
            steps {
                sh 'docker compose up -d --build'
            }
        }
    }
}