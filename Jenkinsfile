@Library('jenkins-shared-library') _

pipeline {
    agent any

    environment {
        IMAGE_NAME = 'ayaahmed123/jenkins-sample'
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
                withCredentials([string(credentialsId: 'dockerhub-cred', variable: 'DOCKER_PASSWORD')]) {
                    pushDockerImage(env.IMAGE_NAME)
                }
            }
        }
    }
}


   
