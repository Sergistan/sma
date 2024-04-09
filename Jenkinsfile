pipeline {
    agent any
    stages {
        stage('Build gradle producer') {
                steps{
                      cdm 'cd producer'
                      cdm './gradlew clean test'
                      cdm './gradlew build'
                }
        }
        stage('Build gradle consumer') {
                steps{
                      cdm 'cd consumer'
                      cdm './gradlew clean test'
                      cdm './gradlew build'
                }
        }
        stage('Build docker image producer') {
            steps{
                    cdm 'docker build -f Dockerfile-producer .'
            }
        }
        stage('Build docker image consumer') {
            steps{
                   cdm 'docker build -f Dockerfile-consumer .'
            }
        }
    }
}