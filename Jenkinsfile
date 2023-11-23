pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Pull the Docker image if not already available
                sh 'docker pull gradle:8.2.0-jdk17-alpine'

                // Run the build commands inside the Docker container
                sh 'docker run --rm -v $PWD:/app -w /app gradle:8.2.0-jdk17-alpine gradle build'
            }
        }
    }
}
