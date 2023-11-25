pipeline {
    agent any

    stages {
        stage('Build Frontend Image') {
            steps {
                script {
                    // Build frontend Docker image
                    docker.build("frontend:latest", "./frontend")
                }
            }
        }

        stage('Build Backend Image') {
            steps {
                script {
                    // Build backend Docker image
                    docker.build("backend:latest", "./backend")
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy frontend and backend to Kubernetes using kubectl run
                    sh "kubectl run frontend --image=frontend:latest --port=80 --expose"
                    sh "kubectl run backend --image=backend:latest --port=3000 --expose"
                }
            }
        }
    }
}
