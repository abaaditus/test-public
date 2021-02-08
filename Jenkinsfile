pipeline {
    agent any
    tools { nodejs "nodejs"}
    stages {
        stage('Pull files'){
            steps {
                echo 'Pulling Jotto..'
                git branch: 'main', credentialsId: '84bd03a8-d6a6-43fc-9a01-6ab100ac3b31', url: 'https://github.com/abaaditus/jotto.git'
            }
        }
        stage('Build'){
            steps {
                echo 'Installing nodeJs modules...'
                sh 'echo $PATH'
                sh 'npm i'
            }
        }
        stage('TEST'){
            steps {
                echo 'Running unit test...'
                sh 'npm run test'
            }
        }
    }
}
