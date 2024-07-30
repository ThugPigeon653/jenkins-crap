pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image from Dockerfile
                    def customImage = docker.build('your-image-name:latest')
                }
            }
        }
        
        stage('Run Container') {
            steps {
                script {
                    // Run commands inside the container
                    docker.image('your-image-name:latest').inside {
                        sh 'hostname'
                    }
                }
            }
        }
    }
}