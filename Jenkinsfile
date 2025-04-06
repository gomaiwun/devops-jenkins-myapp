pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                script {
                    // Build using Maven
                    sh 'mvn clean package'
                }
            }
        }
        stage('Docker') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t myapp .'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Run Docker container
                    sh 'docker run -d -p 8080:8080 myapp'
                }
            }
        }
    }
}
