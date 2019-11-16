pipeline {
    agent any

    stages {
        
        stage('build') {
            steps {
               bat label: '', script: 'mvn install '
            }
        }
        
        
        stage('checkout') {
            steps {
                git 'https://github.com/makremch/integrationTest'
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
