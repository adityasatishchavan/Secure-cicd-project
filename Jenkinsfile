pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Success'
            }
        }

        stage('Test') {
            steps {
                echo 'Test Success'
            }
        }

        stage('Deploy Dev') {
            steps {
                sh 'cp app/index.html dev/'
            }
        }

        stage('Deploy Staging') {
            steps {
                sh 'cp app/index.html staging/'
            }
        }

        stage('Approval') {
            steps {
                input 'Approve Production Deployment?'
            }
        }

        stage('Deploy Prod') {
            steps {
                sh 'cp app/index.html production/'
            }
        }
    }
}
