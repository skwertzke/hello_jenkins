pipeline {
    agent any

    environment {
        PATH = "${tool name: 'Python', type: 'python'}/Scripts:${tool name: 'Python', type: 'python'}/:${env.PATH}"
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
