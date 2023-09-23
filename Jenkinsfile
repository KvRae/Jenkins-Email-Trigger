pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Récupérer le code depuis le dépôt Git
                checkout scm
            }
        }
        stage('Send Email') {
            steps {
                // Envoyer un e-mail avec le contenu d'un fichier
                emailext body: readFile('README.md'), subject: 'Nouveau commit sur GitHub', to: 'karam.mannai@esprit.tn'
            }
        }
    }
}
