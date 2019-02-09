pipeline {
    agent any
    stages {
        stage('myStage'){
      steps {
        sh 'ls -la' 
      }
    }
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}