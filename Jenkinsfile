pipeline {
    agent any

    environment {
        TAG_NAME = 'v1.25'  // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                    withCredentials([string(credentialsId: 'github-http-tokan', variable: 'GITHUB_TOKEN')]) {
                        sh "git tag ${TAG_NAME}"
                        sh "git push --tags "
                    }
                }
            }
        }
    }
}
