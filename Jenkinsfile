pipeline {
    agent any
    tools {
        nodejs 'Node-js' // Ensure this matches the configured name in Jenkins
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
    post {
        always {
            cleanWs() // Clean up the workspace
        }
    }
}
