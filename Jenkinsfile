pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                checkout scm
            }
        }

        stage('Print Environment Variables') {
            steps {
                script {
                    // Print all environment variables to check if PATH is correctly set
                    bat 'C:\\Windows\\System32\\cmd.exe /c set'
                }
            }
        }

        stage('List Files') {
            steps {
                script {
                    // List the files in the workspace to debug paths
                    bat 'C:\\Windows\\System32\\cmd.exe /c dir'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Define the path to the Python executable
                    def pythonPath = 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe'
                    // Run the Python script using cmd.exe
                    bat "C:\\Windows\\System32\\cmd.exe /c \"${pythonPath} hello_jenkins.py\""
                }
            }
        }
    }
}
