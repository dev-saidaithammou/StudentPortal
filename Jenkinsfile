pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/dev-saidaithammou/StudentPortal.git'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Preparing SonarQube analysis...'
            }
        }

        stage('Quality Gate') {
            steps {
                echo 'Checking project quality...'
            }
        }
    }
}