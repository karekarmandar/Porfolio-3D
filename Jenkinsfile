pipeline {
    agent any

    stages {
        /* Let's make sure we have the repository cloned to our workspace */
        stage('Clone repository') {
          steps {
                script {
                    checkout scm
                }
            }
        }
        stage('Build image') {
            steps {
                script {
                   sh 'docker build -t nodejs-portfolio . ' 
            }
        }

    }
}
// python3 app.py
// npm run dev | npm start
