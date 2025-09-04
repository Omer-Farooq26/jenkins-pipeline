pipeline {
    agent any

    stages {
        stage('Greet') {
            steps {
                echo 'Hello Omer, this is a pipeline committed from EC2!'
            }
        }

        stage('Check Docker') {
            steps {
                sh 'docker --version'
                sh 'docker ps'
            }
        }

        stage('List Repo Files') {
            steps {
                sh 'ls -l'
            }
        }
    }
}
