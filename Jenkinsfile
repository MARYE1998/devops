pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs() // Nécessite le plugin "Workspace Cleanup Plugin"
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
}
