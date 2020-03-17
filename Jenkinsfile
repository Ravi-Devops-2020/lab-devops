pipeline {
    agent any
    stages {
        stage('SCM checkout') {
            steps {
                git 'https://github.com/Ravi-Devops-2020/lab-devops.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t chravi2410/my-app:1.0.0 .'
            }
        }
    }
}