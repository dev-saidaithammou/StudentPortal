pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code downloaded from GitHub'
            }
        }

        stage('Code Analysis') {
            steps {
                script {
                    def scannerHome = tool 'SonarScanner'

                    withSonarQubeEnv('SonarQubeServer') {
                        bat "\"${scannerHome}\\bin\\sonar-scanner.bat\" -Dsonar.projectKey=StudentPortal -Dsonar.sources=."
                    }
                }
            }
        }

        stage('Quality Gate') {
            steps {
                echo 'Analysis completed'
            }
        }
    }
}