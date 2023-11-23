pipeline {
    agent any

    stages {
        stage('Pull and Run ARM64 Container') {
            steps {
                script {

                    // Run an interactive ARM64 container
                    sh 'docker run --platform=linux/arm64/v8 ubuntu:latest /bin/bash'
                }
            }
        }
    }
}
