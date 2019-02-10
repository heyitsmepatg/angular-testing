pipeline {
    agent { dockerfile true}
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