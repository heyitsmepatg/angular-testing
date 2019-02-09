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
                sh '''
                    wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
                    sudo dpkg -i google-chrome-stable_current_amd64.deb
                '''
            }
        }
        stage('test') {
            steps {
                sh 'ng test'
            }
        }
    }
}