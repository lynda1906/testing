pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet?')
        string(name: 'Name', defaultValue: 'World', description: 'Who should I greet?')
    }
    options {
        buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '10', numToKeepStr: '10')
        timeout(time: 1, unit: 'HOURS')
    }
    triggers {
        cron('@midnight')
    }
    stages {
        stage('Prep') {
            steps {
                echo 'Stage: Building..'
                sh 'python3 --version'
            }
        }
        stage('Build') {
            steps {
                echo 'Stage: Testing..'
                sh "./script.py ${params.Greeting} ${params.Name}"
            }
        }
        stage('Report') {
            steps {
                echo 'Deploying....'

            }
        }
    }
    post {
        always {
            emailext attachLog: true, body: 'This is a test', subject: 'Testing', to: 'lynda1@managedkaos.com'
       }
/*
        changed { }
        fixed { }
        regression { }
        aborted { }
        failure { }
        success { }
        unstable { }
        cleanup { }
*/
    }
}
