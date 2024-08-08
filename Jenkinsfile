pipeline {
    agent any

    tools {
        // No need to specify python here; use withEnv to set the path directly
    }

    environment {
        PYTHON_HOME = "C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310"
        PATH = "${env.PYTHON_HOME};${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/skwertzke/hello_jenkins.git'
            }
        }
        stage('Run Python Script') {
            steps {
                script {
                    bat '"%PYTHON_HOME%\\python.exe" hello_jenkins.py'
                }
            }
        }
        stage('Archive Results') {
            steps {
                archiveArtifacts artifacts: '**/output.txt', allowEmptyArchive: true
            }
        }
    }
}
