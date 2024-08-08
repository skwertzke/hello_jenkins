pipeline {
    agent any

    tools {
        // Ensure that this name matches the name configured in Jenkins Global Tool Configuration
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
                    bat 'python hello_jenkins.py'
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
