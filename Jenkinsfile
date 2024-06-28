pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                script {
                    // Manually add Python to the PATH
                    // Replace 'C:\\Path\\To\\Python' with the actual installation path of Python on your system
                    env.PATH = "C:\\Program Files\\Python311\\python;C:\\Users\\fatma\\AppData\\Local\\Programs\\Python\\Python311\\Scripts;${env.PATH}"
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Choisissez la commande en fonction de votre script
                    bat'pip install pandas' // Installer les dépendances
                    bat 'python data_analysis.py' // Exécuter le script Python
                
            }
        }
    }
}
}
