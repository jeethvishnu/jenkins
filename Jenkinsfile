pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds() 
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment {
        DEPLOY_TO = 'production'
        GREETING = 'good morning'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo building stage'
                sh 'env'
            }
        }
        stage('Test') {
            steps {
                sh 'echo testing stage'
                sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo deploying'
            }
        }
        stage('print params') {
            steps {
                 echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
                sh 'echo triggered'
            }
             
        }
        
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo 'will run when it is success'
        }
        failure {
            echo 'will run when its failed'
        }
    }
}