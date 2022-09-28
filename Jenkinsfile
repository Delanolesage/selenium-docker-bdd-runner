pipeline {
    agent any
    stages {
        stage("Start Grid"){
            steps {
                bat "docker-compose up -d hub chrome"
            }
        }
        stage("Bring Grid Down"){
            steps {
                bat "docker-compose up ./resources/suite"
            }
        }
        stage("Bring Grid Down"){
            steps {
                bat "docker-compose down"
            }
        }
    }
}