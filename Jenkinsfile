pipeline {
    agent any

    stages {
        stage('Build docker image producer') {
            steps{
                    sh 'docker build -f Dockerfile-producer .'
            }
        }
        stage('Build docker image consumer') {
            steps{
                   sh 'docker build -f Dockerfile-consumer .'
            }
        }
    }
}