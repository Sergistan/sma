pipeline {
    agent any
    stages {
        stage('Build gradle producer') {
                steps{
                    dir('producer') {
                      withGradle {
                      bat './gradlew clean test'
                      bat './gradlew build'
                      }
                    }
                }
        }
        stage('Build gradle consumer') {
                steps{
                    dir('consumer') {
                      withGradle {
                      bat './gradlew clean test'
                      bat './gradlew build'
                      }
                    }
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