pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    bat 'C:\\Users\\dilia\\AppData\\Local\\Programs\\Python\\Python310\\python.exe hello_jenkins.py'
                }
            }
        }
    }
}
