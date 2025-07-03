pipeline {
    agent {
        label 'agent-1'
    } 


stages {
    stage ('build') {
        steps {
            sh 'echo this is build'
        }
    }
    stage ('test') {
        sh 'echo its testing'
    }
    stage ('deploy') {
        sh 'echo deploying'
        sh 'success'
    }
}
}
