pipeline {
    agent any
    environment {
        registry = "srikar1497/pimage"
        registryCredential = "f64cb8ad-a433-4ada-8987-be24f485f188"
        dockerImage = ""
    }
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/yurei14/jenRepo.git']]])
            }
        }
        
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build registry
                }
            }
        }
        
        stage('Pushing to hub') {
            steps {
                script {
                    docker.withRegistry('',registryCredential) {
                        dockerImage.push()
                    }
                }
            }
        }
    }
}
