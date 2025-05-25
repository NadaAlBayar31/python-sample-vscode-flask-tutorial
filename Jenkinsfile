pipeline{
    agent any
        
    
    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t nadaalbayar/data-iti:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push nadaalbayar/data-iti:v${BUILD_NUMBER}"
            }
        }
    }
}
