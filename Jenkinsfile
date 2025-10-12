pipeline {
    agent any
    tools {
        nodejs 'node24.10.0'      // This name must match what you configured in Jenkins
                   // Optional: add JDK if needed
    }
    stages {
        stage('build npm ') {
            steps {
                sh """
                    npm -v
                  
                """
            }
        }

        stage('Build') {
            steps {
                sh """
                    docker build -t docker.io/engy11/ast-test1:v1 .

                    
                """
            }
        }

      stage('Push Docker Image') {
    steps {
        withCredentials([usernamePassword(
            credentialsId: 'docker-cerd',  // <-- ID of your DockerHub credentials in Jenkins
            usernameVariable: 'DOCKER_USER',
            passwordVariable: 'DOCKER_PASS'
        )]) {
            sh '''
                echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
                docker push docker.io/engy11/ast-test1:v1
            '''
        }
    }
}

    }

   
}
