pipeline {
    agent any

    stages {
        stage('Pull and Run ARM64 Container') {
            steps {
                script {
                    // Run apt update and upgrade inside the ARM64 container
                    sh 'docker run --rm --platform=linux/arm64/v8 ubuntu:latest /bin/bash -c "apt update && apt upgrade -y"'
                }
            }
        }
    }
}
