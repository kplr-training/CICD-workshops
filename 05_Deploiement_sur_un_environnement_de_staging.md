Objectif: Déployer l'application sur un environnement de staging pour les tests supplémentaires.

1. Ajoutez une étape de déploiement sur un environnement de staging.

`Jenkinsfile`:


```Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the application"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests"'
            }
        }
        stage('Deploy Staging') {
            steps {
                sh 'echo "Deploying to staging"'
            }
        }
    }
}

```

- Une étape "Deploy Staging" a été ajoutée pour simuler le déploiement de l'application sur un environnement de staging.
    
- `sh 'echo "Deploying to staging"'`: Cette ligne simule le déploiement sur un environnement de staging. Vous devrez remplacer cette ligne par les commandes réelles de déploiement sur votre environnement de staging.