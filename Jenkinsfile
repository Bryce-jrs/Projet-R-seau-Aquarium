pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://ton-repo.git'
            }
        }

        stage('Clean') {
            steps {
                sh 'make clean'
            }
        }

        stage('Build server') {
            steps {
                sh 'make server'
            }
        }

        stage('Build tests') {
            steps {
                sh 'make test'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'server,test_*', fingerprint: true
        }
    }
}
