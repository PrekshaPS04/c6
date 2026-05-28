pipleline {
    agent any
    stages{
        stage('Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run App') {
            steps {
                bat 'node app.js'
            }
        }
        stage('Test') {
            steps {
                bat 'node test.js'
            }
        }
        stage('Build') {
            steps {
                bat 'docker build -t c6 .'
            }
        }
        stage('Run container') {
            steps {
                bat 'docker run -d -p 3000:3000 --name c7 c6'
            }
        }
    }
}