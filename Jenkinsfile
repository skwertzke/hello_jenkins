pipeline {
    agent any

    tools {
        python 'Python' // Ensure this matches the name in Jenkins Global Tool Configuration
    }

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
                    sh 'python hello_jenkins.py'
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
