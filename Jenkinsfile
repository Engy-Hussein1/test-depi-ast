pipeline {
    agent any
    tools {
        nodejs 'node24.10.0'      // This name must match what you configured in Jenkins
                   // Optional: add JDK if needed
    }
    stages {
        stage('Login') {
            steps {
                sh """
                    npm -v
                  
                """
            }
        }

        stage('Build') {
            steps {
                sh """
                    echo "Building the project..."
                   
                """
            }
        }

        stage('Deploy') {
            steps {
                sh """
                    echo "Deploying the project..."
                   
                """
            }
        }
    }

   
}
