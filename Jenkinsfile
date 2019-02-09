pipeline {
    agent {
        docker {
            image 'node:6-alpine'
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
            }
        }
        stage('test') {
            steps {
                sh 'ng test'
            }
        }
    }
}