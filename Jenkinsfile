pipeline {
    agent any
    stages {
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
        stage('Build docker image consumer') {
            steps{
                   bat 'docker build -f Dockerfile-consumer .'
            }
        }
    }
}