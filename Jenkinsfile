pipeline {
    agent {
        docker {
            image 'python:3.11.4-alpine'
        }
    }
    stages {
        stage('Workspace Cleanup') {
            steps {
                deleteDir()
            }
        }
        stage('Fetch Repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'br1']], 
                          userRemoteConfigs: [[url: 'https://github.com/nohhyejin1/jenkins_first.git']]])
            }
        }
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