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
        // building docker image 
        stage('Build image') {
            steps {
                script {
                   sh 'docker build -t nodejs-portfolio . ' 
                }
            }

        }
        // running docker containers 
        stage('Running the Container') {
            steps {
                script {
                   sh ' dokcer stop portfolio-con && docker rm portfolio-con && docker run -d --name portfolio-con -p 80:8080 nodejs-portfolio' 
                }
            }

        }
    }
}
// python3 app.py
// npm run dev | npm start
