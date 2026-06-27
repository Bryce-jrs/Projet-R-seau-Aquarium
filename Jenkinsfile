pipeline {
    agent any

    stages {
        stage('Build server') {
            steps {
                sh '''
                        sudo apt update
                        sudo apt install -y make
                        make clean
                        make all
                    '''
            }
        }
    }
}
