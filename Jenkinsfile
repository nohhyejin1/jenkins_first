pipeline {
    agent {
        docker {
            image 'python:3.11.4-alpine'
        }
    }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
    post {
        always {
            echp "Always, success or not"
        }
    }
}