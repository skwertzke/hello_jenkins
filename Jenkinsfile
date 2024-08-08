pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Ensure Python is installed and accessible
                    def python = tool name: 'Python 3.x', type: 'Python'
                    bat "${python}/python hello_jenkins.py"
                }
            }
        }

        stage('Archive Results') {
            steps {
                archiveArtifacts artifacts: 'output.txt'
            }
        }
    }
}
