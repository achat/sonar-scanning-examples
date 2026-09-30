pipeline {
    agent any

    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'sonar-scanner -Dsonar.projectKey=sonar-scanning-examples -Dsonar.sources=.'
                }
            }
        }
    }
}
