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
                echo 'Deploying to Dev Environment'
            }
        }

        stage('Deploy Staging') {
            steps {
                echo 'Deploying to Staging Environment'
            }
        }

        stage('Manual Approval') {
            steps {
                input 'Approve Production Deployment?'
            }
        }

        stage('Deploy Production') {
            steps {
                echo 'Deploying to Production Environment'
            }
        }
    }
}
