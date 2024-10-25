pipeline {
    agent any
    stages {
        stage('Clonage du dépôt GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/theo-riou/workflows'
            }
        }
        stage('Installation des dépendances') {
            steps {
                script {
                    sh 'python3 -m pip install --upgrade pip'
                    sh 'python3 -m pip install -r requirements.txt'
                }
            }
        }
        stage('Exécution des tests') {
            steps {
                sh 'python3 -m pytest'
            }
        }
    }
}
