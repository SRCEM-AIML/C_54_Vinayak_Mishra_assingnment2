pipeline {
    agent any

    environment {
        IMAGE_NAME = 'vinayakmishra11/studentproject'
        CONTAINER_NAME = 'studentproject'
    }

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    git branch: 'main',
                        credentialsId: 'github-credentials',
                        url: 'https://github.com/SRCEM-AIML/C_54_Vinayak_Mishra_assingnment2.git'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                bat "docker build -t %IMAGE_NAME% ."
            }
        }

        stage('Push to Docker Hub') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                        bat """
                        echo %DOCKER_PASS% | docker login -u %DOCKER_USER% --password-stdin
                        docker push %IMAGE_NAME%
                        """
                    }
                }
            }
        }
    }
}
