pipeline {
    agent any
    environment{
        JAVA_HOME ='C:\\Program Files\\Java\\jdk-21'
        PYTHON_HOME ='c:\users\fatma\appdata\local\programs\python\python311'
        PATH = "${env.PATH};${env.JAVA_HOME}\\bin;${env.PYTHON_HOME};${env.PYTHON_HOME}\\Scripts"
    }
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

