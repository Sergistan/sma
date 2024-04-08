pipeline {
    agent any

    tools {
        jdk "17"
        gradle "8.5"
    }

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