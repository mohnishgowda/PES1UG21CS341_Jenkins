pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling the C++ file...'
                    sh "g++ -o PES1UG21CS341-1 PES1UG21CS341.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                scpt {
                    echo 'Running the C++ program...'
                    sh "./PES1UG21CS341-1"
                }
            }
        }

        stage('Deploy') {
            steps {
                 echo 'Deployment stage'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
