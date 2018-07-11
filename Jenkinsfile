pipeline {
    agent any
    parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet?')
        string(name: 'Name', defaultValue: 'World', description: 'Who should I greet?')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Stage: Building..'
                sh 'python3 --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Stage: Testing..'
                sh "./script.py ${params.Greeting} ${params.Name}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
