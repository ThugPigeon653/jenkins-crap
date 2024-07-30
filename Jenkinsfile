pipeline {
    agent { label 'dev' }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build'){
            steps {
                script {
                    sh 'docker build -t dockerimage .'
                }
            }
        }
    }
}