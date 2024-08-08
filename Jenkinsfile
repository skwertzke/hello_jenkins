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
                    // Print PATH variable using PowerShell
                    bat 'powershell -Command "Write-Output $env:PATH"'
                }
            }
        }

        stage('Verify CMD Path') {
            steps {
                script {
                    // Verify cmd.exe location using PowerShell
                    bat 'powershell -Command "Get-Command cmd.exe | Select-Object Source"'
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
