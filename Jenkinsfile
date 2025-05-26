pipeline {
    agent any

    environment {
        IMAGE_NAME = 'nadaalbayar/jenkins-sample'
    }

    stages {
        stage('Build Python App') {
            steps {
                buildPythonApp()
            }
        }

        stage('Build Docker Image') {
            steps {
                buildDockerImage(env.IMAGE_NAME)
            }
        }

        stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'docker-hub-access', 
                    usernameVariable: 'DOCKER_USER', 
                    passwordVariable: 'DOCKER_PASSWORD'
                )]) {
                    pushDockerImage(env.IMAGE_NAME)
                }
            }
        }
    }
}



   
