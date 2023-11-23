pipeline {
    agent any

    stages {
        stage('Setup QEMU and Docker') {
            steps {
                script {

                    // Enable QEMU for ARM64 binaries
                   // sh 'sudo update-binfmts --enable qemu-aarch64'

                    // Install Docker multi-architecture support
                    sh 'docker run --rm --privileged multiarch/qemu-user-static --reset -p yes'
                }
            }
        }
        stage('Pull and Run ARM64 Container') {
            steps {
                script {
                    // Pull the ARM64-based Ubuntu image
                    sh 'docker pull --platform=linux/arm64/v8 ubuntu:latest'

                    // Run an interactive ARM64 container
                    sh 'docker run --platform=linux/arm64/v8 -it ubuntu:latest /bin/bash'
                }
            }
        }
    }
}
