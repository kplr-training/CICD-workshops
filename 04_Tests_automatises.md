Objectif: Intégrer des tests automatisés dans le pipeline pour vérifier la qualité du code.

1. Ajoutez une étape de test après la construction.

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
    }
}

```

- Encore une fois, ce code est similaire à l'atelier 1, avec une nouvelle étape "Test" ajoutée.
    
- `sh 'echo "Running tests"'`: Cette ligne simule l'exécution des tests automatisés de l'application. Vous devriez remplacer cette ligne par les commandes réelles nécessaires pour exécuter les tests de votre application.
