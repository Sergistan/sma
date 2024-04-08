pipeline {
    agent any

    stages {
        stage('Build gradle producer') {
                steps{
                      sh 'cd producer'
                      sh './gradlew build'
                }
        }
        stage('Build gradle consumer') {
                steps{
                      sh 'cd consumer'
                      sh './gradlew build'
                }
        }
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