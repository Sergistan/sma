pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps{
                git branch: 'main',
                    url: 'https://github.com/Sergistan/sma.git'
                }
        }

//         stage('Build docker image') {
//             steps{
//                 dir('lesson-1') {
//                     sh 'docker build -t bakavets/jenkins-images:0.4 .'
//                 }
//             }
//         }
    }
}