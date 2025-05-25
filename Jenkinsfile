pipeline{
    agent any
        
    
    stages{
        stage("build Docker image"){
            steps{
                sh "docker build -t nadaalbayar/welnaby:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push nadaalbayar/welnaby:v${BUILD_NUMBER}"
            }
        }
    }
}
