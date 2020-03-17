pipeline {
    agent any

    stages {
        stage('SCM checkout') {
            steps {
                git 'https://github.com/Ravi-Devops-2020/lab-devops.git'
				echo 'SCM checkout..'
            }
        }
        stage('Build') {
            steps {
                echo 'Building an image..'
            }
        }
        stage('Publish') {
            steps {
                echo 'Publishing to repo....'
            }
        }
    }
}