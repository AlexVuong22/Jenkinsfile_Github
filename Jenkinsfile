pipeline {
    agent any

    environment {
        GIT_CREDENTIALS = credentials('admin12345')
    }

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'admin12345', url: 'git@github.com:AlexVuong22/Jenkinsfile_Github.git'
            }
        }
    }
}
