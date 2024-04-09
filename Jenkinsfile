pipeline {
    agent any
    stages {
        stage('Build gradle producer') {
                steps{
                    dir('producer') {
                      withGradle {
                      bat './gradlew clean'
                      bat './gradlew build'
                      }
                    }
                }
        }
        stage('Build gradle consumer') {
                steps{
                    dir('consumer') {
                      withGradle {
                      bat './gradlew clean'
                      bat './gradlew build'
                      }
                    }
                }
        }
        stage('Build docker image producer') {
            steps{
                    dir('producer') {
                    bat 'docker build .'
                    }
            }
        }
        stage('Build docker image consumer') {
            steps{
                    dir('consumer') {
                    bat 'docker build .'
                    }
            }
        }
    }
}