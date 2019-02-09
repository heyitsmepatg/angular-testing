pipeline {
    agent {
        docker {
            image 'node:11.9.0-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('myStage') {
            steps {
                sh 'ls -la' 
            }
        }
        stage('build') {
            steps {
                sh 'npm install'
                sh 'npm install -g @angular/cli'
                sh 'export CHROME_BIN=/usr/bin/chromium-browser'
            }
        }
        stage('test') {
            steps {
                sh 'ng test'
            }
        }
    }
}