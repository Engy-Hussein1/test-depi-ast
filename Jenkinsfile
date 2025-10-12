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

        // stage('push image ') {
        //     steps {
        //         sh """
        //             docker login -u  engy11  -p 
                   
        //         """
        //     }
        // }
    }

   
}
