pipeline {
    agent any
    environment{
        JAVA_HOME = 'C:\\Program Files\\Java\\jdk1.8.0_202'
        PYTHON_HOME = 'C:\\Users\\rehou\\AppData\\Local\\Programs\\Python\\Python39-32'
        PATH = "${env.PATH};${env.JAVA_HOME}\\bin;${env.PYTHON_HOME}"};${env.PYTHON_HOME}"}\\Scripts"
    stages {
        
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
