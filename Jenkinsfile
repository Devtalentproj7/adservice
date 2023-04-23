pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Devtalentproj7/adservice.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            // Clean up the workspace
            cleanWs()
        }
    }
}
