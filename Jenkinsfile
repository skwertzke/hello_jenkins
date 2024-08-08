pipeline {
    agent any

    tools {
        // This should be the name configured in Global Tool Configuration
        python 'Python' 
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
                    // Make sure Python is available on PATH or specify full path
                    bat '"C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" hello_jenkins.py'
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
