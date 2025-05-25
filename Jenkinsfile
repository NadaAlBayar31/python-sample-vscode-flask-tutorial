node {
    

    stage('Checkout') {
        checkout scm
    }

    stage('Build Image') {
         sh "docker build -t nadaalbayar/welnaby:v${BUILD_NUMBER} ."
    }

    stage('Push Image') {
         sh "docker push nadaalbayar/welnaby:v${BUILD_NUMBER}"
            
        }
    }

   
