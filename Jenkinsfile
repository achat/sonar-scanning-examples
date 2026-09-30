pipeline {
    agent none

    stages {

        stage('SonarQube Analysis') {
            agent {
                docker {
                    image 'sonarsource/sonar-scanner-cli:latest'
                    reuseNode true
                }
            }

            steps {
                withSonarQubeEnv('SonarQube') {
                    sh '''
                        sonar-scanner \
                          -Dsonar.projectKey=sonar-scanning-examples \
                          -Dsonar.projectName=sonar-scanning-examples \
                          -Dsonar.sources=.
                    '''
                }
            }
        }
    }
}
```
