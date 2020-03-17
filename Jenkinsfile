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
        stage('Push Docker Image') {
			withCredentials([string(credentialsId: 'docker-pwd', variable: 'dockerHubPwd')]) {
			sh "docker login -u chravi2410 -p ${dockerHubPwd}"
			}
            steps {
                
				sh 'docker push chravi2410/my-app:1.0.0'
            }
        }
    }
}