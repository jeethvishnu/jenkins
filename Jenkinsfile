pipeline {
    agent {
        label 'agent-1'
    } 


stages {
    stage ('build') {
        steps {
            sh 'echo building'
        }
    }
    stage ('test') {
        steps {
            sh 'echo testing'
        }
    }
    stage ('deploy') {
        steps {
            sh 'echo deploying'
        }
    }
}
}