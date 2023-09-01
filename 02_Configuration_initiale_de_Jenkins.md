
Ces ateliers (de 02 à 06) décrivent les étapes de base pour créer un pipeline CI/CD avec Jenkins pour une application Python simple. Vous pouvez personnaliser davantage chaque étape en fonction de vos besoins et des outils spécifiques que vous utilisez pour le déploiement, les tests et autres actions.

Objectif: Configurer Jenkins pour commencer à travailler sur des pipelines CI/CD.

1. Installez Jenkins et lancez-le.
2. Accédez à l'interface Jenkins via votre navigateur.
3. Installez le plugin "Pipeline" si ce n'est pas déjà fait.
4. Créez un nouveau pipeline dans Jenkins.
5. Utilisez le fichier `Jenkinsfile` pour définir les étapes de base du pipeline.

`Jenkinsfile`:

```Jenkinsfile
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building the application"'
            }
        }
    }
}
```

- `pipeline {`: Cette ligne indique le début de la définition du pipeline Jenkins.
    
- `agent any`: Cette ligne spécifie que le pipeline peut être exécuté sur n'importe quel agent (nœud Jenkins) disponible.
    
- `stages {`: C'est le début de la section où vous définissez les différentes étapes du pipeline.
    
- `stage('Build') {`: Ceci commence la définition d'une étape nommée "Build". Vous pouvez donner un nom descriptif à chaque étape.
    
- `steps {`: Les actions à effectuer dans cette étape sont définies dans cette section.
    
- `sh 'echo "Building the application"'`: Cette ligne utilise la commande shell (`sh`) pour exécuter une simple commande d'impression qui simule la construction de l'application. Vous pouvez remplacer cette commande par les commandes réelles de construction de votre application Python.
