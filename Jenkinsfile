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
                    // Print PATH variable directly using cmd.exe with full path
                    bat 'C:\\Windows\\System32\\cmd.exe /c echo %PATH%'
                }
            }
        }

        stage('Verify CMD Path') {
            steps {
                script {
                    // Verify cmd.exe location directly using full path
                    bat 'C:\\Windows\\System32\\cmd.exe /c where cmd'
                }
            }
        }

        stage('List Files') {
            steps {
                script {
                    // List files in the workspace directly using PowerShell
                    bat 'powershell -Command "Get-ChildItem"'
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Specify the full path to the Python executable and script
                    def pythonPath = 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe'
                    def scriptPath = 'C:\\ProgramData\\Jenkins\\.jenkins\\workspace\\hello_jenkins\\hello_jenkins.py'
                    // Run the Python script directly using the full path to Python
                    bat "\"${pythonPath}\" \"${scriptPath}\""
                }
            }
        }
    }
}
