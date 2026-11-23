pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code already downloaded from GitHub'
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