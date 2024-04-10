pipeline {
    agent any
    stages {
        // stage('Build') {
        //     steps {
        //         //
        //     }
        // }
        stage('Deploy') {
            steps {
                sh 'docker-compose build'
                sh 'docker compose up -d'
            }
        }
    }
}
