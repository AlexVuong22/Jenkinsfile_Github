pipeline {
    agent any

    environment {
        GIT_CREDENTIALS = credentials('admin12345')
    }

    stages {
        stage('Credentials') {
            steps {
                script {
                    withCredentials([gitUsernamePassword(credentialsId: 'admin12345', gitToolName: 'Default')]) {
                    // some block
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
