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
                
            }
        }
    }
}