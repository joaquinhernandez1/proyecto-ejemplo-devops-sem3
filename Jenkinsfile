pipeline {
    agent any
    stages {
        stage('Step 1: Clonar repositorio') {
            steps {
                git branch: 'master', url: 'https://github.com/joaquinhernandez1/proyecto-ejemplo-devops-sem3.git'
            }
        }
        stage('Step 2: Ejecutar comandos basicos') {
            steps {
                script {
                    sh 'echo "Running basic commands..."'
                    sh 'ls -la'
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline completado exitosamente.'
            cleanWs()
        }
    }
}
