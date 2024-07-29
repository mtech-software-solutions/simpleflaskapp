pipeline {
    agent any
    environment {
        DOCKER_LOGIN=credentials('DOCKER_LOGIN')
    }
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker compose build'
                sh 'sudo docker login -u ${DOCKER_LOGIN_USR} -p ${DOCKER_LOGIN_PSW}'
                sh 'sudo docker compose push'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo docker compose up -d'
            }
        }
    }
}
