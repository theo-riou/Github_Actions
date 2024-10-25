pipeline {
    agent any

    stages {
        stage('Clonage du dépôt GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/theo-riou/workflows.git'
            }
        }

        stage('Installer les dépendances') {
            steps {
                script {
                    sh 'python -m pip install --upgrade pip'
                    sh 'pip install -r requirements.txt'
                }
            }
        }

        stage('Exécuter les tests') {
            steps {
                script {
                    sh 'pytest'
                }
            }
        }
    }
}
