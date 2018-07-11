pipeline {
    agent any

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
                sh './script.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
