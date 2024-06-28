pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                script {
                    // Manually add Python to the PATH
                    // Replace 'C:\\Path\\To\\Python' with the actual installation path of Python on your system
                    env.PATH = "C:\\Program Files\\Python311\\python;C:\\Program Files\\Python311\\python\\Scripts;${env.PATH}"
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Create a virtual environment
                    bat 'python -m venv venv'

                    // Activate the virtual environment and install dependencies
                    bat '''
                    venv\\Scripts\\activate
                    && pip install --upgrade pip
                    && pip install pandas
                    '''

                    // Run the Python script
                    bat '''
                    venv\\Scripts\\activate
                    && python data_analysis.py
                    '''
                }
            }
        }
    }
}
