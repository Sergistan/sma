pipeline {
    agent any

    stages {
        stage('Build gradle producer') {
                steps{
                      bat 'cd producer'
                      bat './gradlew clean test'
                      bat './gradlew build'
                }
        }
        stage('Build gradle consumer') {
                steps{
                      bat 'cd consumer'
                      bat './gradlew clean test'
                      bat './gradlew build'
                }
        }
        stage('Build docker image producer') {
            steps{
                    bat 'docker build -f Dockerfile-producer .'
            }
        }
        stage('Build docker image consumer') {
            steps{
                   bat 'docker build -f Dockerfile-consumer .'
            }
        }
    }
}