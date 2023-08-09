pipeline {
    agent any

    environment {
        TAG_NAME = 'v1.0.0'  // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                    withCredentials([string(credentialsId: 'github-token', variable: 'GITHUB_TOKEN')]) {
                        sh "git config --global user.email 'jenkins@example.com'"
                        sh "git config --global user.name 'Jenkins'"
                        sh "git tag ${TAG_NAME}"
                        sh "git push --tags "
                    }
                }
            }
        }
    }
}
