pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Ensure the Python executable path is correct
                    def pythonPath = 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe'
                    // Run the Python script
                    bat "${pythonPath} hello_jenkins.py"
                }
            }
        }
    }
}
