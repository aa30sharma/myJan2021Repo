pipeline {
    agent any

    environment {
        TAG_NAME = 'v1.27'  // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                   withCredentials([usernameColonPassword(credentialsId: 'gitCred', variable: 'GITHUB_TOKEN')]) {
                        sh "git config --global user.name 'aa30sharma'"
                        sh "git config --global user.email 'sharmaaatish552@gmail.com'"
                        sh "git tag -a ${TAG_NAME} -m 'lol' "
                        sh "git push -u origin main "
                    }
                }
            }
        }
    }
}
