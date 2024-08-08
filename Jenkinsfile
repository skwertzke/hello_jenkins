pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Run the Python script
                    bat 'python hello_jenkins.py' // For Windows
                }
            }
        }

        stage('Archive Results') {
            steps {
                // Archive any results or artifacts if needed
                archiveArtifacts artifacts: '**/*.log', allowEmptyArchive: true
            }
        }
    }
}
