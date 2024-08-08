pipeline {
    agent any

    tools {
        python 'Python' // Make sure 'Python' matches the name in the Global Tool Configuration
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    def pythonPath = tool name: 'Python', type: 'PythonInstallation'
                    bat "${pythonPath}/python.exe hello_jenkins.py"
                }
            }
        }
    }
}
