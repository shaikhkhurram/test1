pipeline {
    agent any

    tools {
        maven 'Maven 3.9.6' // Name must match the Maven installation name in Jenkins
    }

    triggers {
        pollSCM('* * * * *') // or use webhook from GitHub for auto-trigger
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging...'
                sh 'mvn package'
            }
        }
    }
}
