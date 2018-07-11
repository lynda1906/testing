pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Stage: Building..'
                sh 'python -v'
            }
        }
        stage('Test') {
            steps {
                echo 'Stage: Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
