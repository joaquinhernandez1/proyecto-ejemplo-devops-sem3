pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://git.utec.edu.uy/joaquin.hernandez/trabajo-individual-foro-rick-y-morty.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('rick-morty-api-docker').inside {
                        echo 'Docker container is up and running!'
                    }
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}
