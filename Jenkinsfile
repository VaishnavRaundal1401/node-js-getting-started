pipeline {
    agent any

    tools {
        nodejs 'NodeJS'  // Ensure this name matches the NodeJS tool installation in Jenkins
    }

    environment {
        PATH = "${tool 'NodeJS'}/bin:${env.PATH}"  // Correct way to set PATH
    }

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'npm start'
            }
        }
    }
}
