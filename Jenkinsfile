pipeline {
    agent any
    
    environment {
        CXX = 'g++'
        SRN = 'PES2UG21CS283-1'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling C++ application'
                    sh "${CXX} -o my_app main.cpp"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running C++ application'
                    sh './my_app'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage (if needed)'
                // Add deployment steps here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
