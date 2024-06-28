pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                script {
                    // Ensure Python is in the PATH
                    def pythonHome = tool name: 'Python 3.9', type: 'Python'
                    env.PATH = "${pythonHome}/Scripts:${pythonHome}:${env.PATH}"
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
