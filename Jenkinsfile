pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                checkout scm
            }
        }

        stage('List Files') {
            steps {
                script {
                    // List the files in the workspace to debug paths
                    bat 'dir'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Define the path to the Python executable
                    def pythonPath = 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe'
                    // Run the Python script
                    bat "${pythonPath} hello_jenkins.py"
                }
            }
        }
    }
}
