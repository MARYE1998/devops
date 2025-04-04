pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs() // Supprime tous les fichiers présents dans le répertoire de travail Jenkins avant de commencer un nouveau build, pour éviter les conflits ou erreurs dues à d’anciens fichiers.
            }
        }

        stage('Checkout Code') {
            steps {
                git credentialsId: 'PAT_jenkins', url: 'https://github.com/MARYE1998/devops.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
    

