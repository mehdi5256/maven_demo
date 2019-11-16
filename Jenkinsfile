pipeline {
    agent any

    stages {
        
        stage('build') {
            steps {
               bat label: '', script: 'mvn install deploy '
            }
        }
        
        
        stage('checkout') {
            steps {
                git 'https://github.com/mehdi5256/maven_demo'
            }
        }
        stage('Test') {
            steps {
                bat label: '', script: 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
