pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Build Success'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Unit Test Success'
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

        stage('Deploy Production') {
            steps {
                sh 'cp app/index.html production/'
            }
        }
    }
}
