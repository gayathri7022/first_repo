pipeline {
    agent any

    stages {
        stage('Checkout code') {
            steps {
                git credentialsId : 'MY_PAT', url : 'https://github.com/gayathri7022/first_repo.git', branch : 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat '''
                    "C:\\Users\\mjmnj\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m venv venv
                    call .\\venv\\Scripts\\activate
                    pip install --upgrade pip
                    pip install pytest
                '''
            }
        }

        stage ('Test') {
            steps {
                bat '''
                call .\\venv\\Scripts\\activate
                pytest test.py
                '''
            }
                
        }

        stage ('Deploy') {
            steps {
                echo "Deploying Feature"
                bat '''
                call .\\venv\\Scripts\\activate
                "C:\\Users\\mjmnj\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" add.py
                '''
            }
        }
    }
}