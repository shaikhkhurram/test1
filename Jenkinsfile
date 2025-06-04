pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // or use webhook from GitHub for auto-trigger
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging...'
                bat 'mvn package'
            }
        }
    }
}
