pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    // Assuming your C++ file is named main.cpp
                    sh 'g++ -o output PES1UG21CS136.cpp'
                    echo 'Build Stage Successful' // Compile the .cpp file
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './output'
                    echo 'Test Stage Successful' // Execute the compiled binary
                }
            }
        }
        
        stage('Deploy') {
            steps {
               echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
            // You can add additional actions in case of failure
        }
    }
}
