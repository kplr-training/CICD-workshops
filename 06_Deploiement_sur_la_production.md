
Objectif: Déployer l'application sur l'environnement de production après les tests réussis.

1. Ajoutez une étape de déploiement sur l'environnement de production après le déploiement sur le staging.

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
        stage('Deploy Production') {
            steps {
                sh 'echo "Deploying to production"'
            }
        }
    }
}

```

- Dans cet atelier, une étape "Deploy Production" a été ajoutée pour simuler le déploiement sur l'environnement de production.
    
- `sh 'echo "Deploying to production"'`: Cette ligne simule le déploiement sur l'environnement de production. Vous devrez remplacer cette ligne par les commandes réelles de déploiement sur votre environnement de production.
