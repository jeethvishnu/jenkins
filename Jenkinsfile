pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo building stage'
            }
        }
        stage('Test') {
            steps {
                sh 'testing stage'
            }
        }
        stage('Deploy') {
            steps {
                sh 'deploying'
            }
        }
    }
}