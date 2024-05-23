pipeline {
    agent any

    environment {
        MY_CREDENTIALS = credentials(admin12345)
    }

    stages {
        stage('Credentials') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'admin12345', usernameVariable: 'admin', passwordVariable: 'password')]) {
                        sh "echo 'Username: admin'"
                        sh "echo 'Password: password'"
                    }
                }
            }
        }

        stage('Clone') {
            steps {
                git 'git@github.com:AlexVuong22/Jenkinsfile_Github.git'
            }
        }
    }
}
