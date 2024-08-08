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
                    // Print the PATH variable to verify it's correctly set
                    bat 'echo %PATH%'
                    
                    // List files in the workspace to verify the contents
                    bat 'dir'
                    
                    // Verify that cmd is accessible
                    bat 'C:\\Windows\\System32\\cmd.exe /c echo Hello'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Define the path to the Python executable
                    def pythonPath = 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe'
                    
                    // Print the Python path to verify it's correct
                    bat "echo Python Path: ${pythonPath}"
                    
                    // Run the Python script
                    bat "${pythonPath} hello_jenkins.py"
                }
            }
        }
    }
}
