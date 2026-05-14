pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Code cloned successfully'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mywebsite .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8090:80 --name mycontainer mywebsite'
            }
        }

    }
}
