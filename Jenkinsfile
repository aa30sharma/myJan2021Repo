pipeline {
    agent any

    environment {
        TAG_NAME = 'v1.25'  // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                   withCredentials([usernameColonPassword(credentialsId: 'gitCred', variable: 'GITHUB_TOKEN')]) {
                        sh "git config --global user.name 'aa30sharma'"
                        sh "git config --global user.email 'sharmaaatish552@gmail.com'"
                        sh "git tag ${TAG_NAME}"
                        sh "git push --tags "
                    }
                }
            }
        }
    }
}
