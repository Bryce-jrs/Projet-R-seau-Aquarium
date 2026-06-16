pipeline {
    agent any

    stages {

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
