Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { docker { image 'node:6.2' } }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
            }
        }
    }
}