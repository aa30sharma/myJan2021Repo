pipeline {
    agent any

    environment {
        TAG_NAME = 'v1.23'  // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                    withCredentials([string(credentialsId: 'github-http-tokan', variable: 'GITHUB_TOKEN')]) {
                        sh "git config --global user.email 'sharmaaatish552@gmail.com'"
                        sh "git config --global user.name 'aa30sharma'"
                        sh "git tag ${TAG_NAME}"
                        sh "git push --tags "
                    }
                }
            }
        }
    }
}
