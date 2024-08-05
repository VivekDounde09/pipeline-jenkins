pipeline {
    agent any
    tools { 
        nodejs "NodeJS_Installation_Name" // Replace with the name of your Node.js installation in Jenkins Global Tool Configuration
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from your Git repository
                git 'https://github.com/VivekDounde09/pipeline-jenkins.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Run npm install to install dependencies
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                // Run npm run build to build the project
                sh 'npm run build'
            }
        }
    }
    post {
        always {
            // Actions to take regardless of build result
            echo 'Cleaning up workspace...'
            deleteDir() // Clean up the workspace
        }
        success {
            // Actions to take on successful build
            echo 'Build succeeded!'
        }
        failure {
            // Actions to take on failed build
            echo 'Build failed!'
        }
    }
}
