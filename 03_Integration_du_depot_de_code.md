
Objectif: Intégrer le dépôt de code avec Jenkins et déclencher automatiquement le pipeline lors de nouvelles modifications.

1. Connectez-vous au dépôt de code (par exemple, GitHub) et configurez un webhook pour notifier Jenkins des modifications.
2. Mettez à jour le `Jenkinsfile` pour ajouter une étape de récupération du code depuis le dépôt.

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
    }
}

```

- Ce code est similaire à l'atelier 1, à l'exception de l'étape "Checkout" ajoutée.
    
- `checkout scm`: Cette ligne permet à Jenkins de récupérer le code source depuis le système de contrôle de version (SCM) configuré, tel que Git. Cela permet d'obtenir la dernière version du code avant de procéder à la construction.