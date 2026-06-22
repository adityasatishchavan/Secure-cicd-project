pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Successful'
            }
        }

        stage('Unit Test') {
            steps {
                echo 'Unit Test Successful'
            }
        }

        stage('Deploy Dev') {
            steps {
                sh '''
                mkdir -p dev
                cp app/index.html dev/
                '''
            }
        }

        stage('Deploy Staging') {
            steps {
                sh '''
                mkdir -p staging
                cp app/index.html staging/
                '''
            }
        }

        stage('Approval') {
            steps {
                input message: 'Approve Deployment to Production?'
            }
        }

        stage('Deploy Production') {
            steps {
                sh '''
                mkdir -p production
                cp app/index.html production/
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline Completed Successfully 🎉'
        }

        failure {
            echo 'Pipeline Failed ❌ Check logs'
        }
    }
}
