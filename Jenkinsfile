pipeline {
    agent any

    environment {
        TAG_NAME = "v1.${env.BUILD_ID}" // Replace with your desired tag name
    }

    stages {

        stage('Push Tag') {
            steps {
                script {
                   withCredentials([usernameColonPassword(credentialsId: 'gitCred', variable: 'GITHUB_TOKEN')]) {
                       sh "git clone https://github.com/aa30sharma/myJan2021Repo.git "
                       // sh "git config --global user.name 'aa30sharma'"
                      //  sh "git config --global user.email 'sharmaaatish552@gmail.com'"
                      //  sh "ls"
                      //  sh "git add . " 
                      //  sh "git commit -m 'lol' "
                       // sh "git push origin main "
                    }
                }
            }
        }
    }
}
