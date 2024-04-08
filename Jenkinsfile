pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps{
                git branch: 'main',
                    url: 'https://github.com/Sergistan/sma.git'
                }
        }
    }
}