pipeline {
    agent any
    stages {
        stage('Build gradle producer') {
                steps{
                    dir('producer') {
                      withGradle {
                      sh './gradlew clean test'
                      sh './gradlew build'
                      }
                    }
                }
        }
        stage('Build gradle consumer') {
                steps{
                    dir('consumer') {
                      withGradle {
                      sh './gradlew clean test'
                      sh './gradlew build'
                      }
                    }
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