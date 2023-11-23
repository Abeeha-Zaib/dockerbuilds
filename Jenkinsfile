pipeline {
    agent any
    stages {
        stage('Arm Container') {
            steps {
                // Pull the Docker image if not already available
                sh 'docker pull --platform=linux/arm64 ubuntu:latest'
            
                // Run the build commands inside the Docker container
                sh 'docker run --platform=linux/arm64 ubuntu:latest /bin/bash'
            }
        }
    }
}
