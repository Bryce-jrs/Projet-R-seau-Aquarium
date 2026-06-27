pipeline {
    agent any

    stages {
        stage('Build server') {
            steps {
                sh '''
                    make clean && make all  
                '''
            }
        }
    }
}
