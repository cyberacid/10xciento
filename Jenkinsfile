pipeline {
    agent any
    stages {
        stage('Clean') {
            steps {
                sh "mvn clean"
            }
        }

        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }

        stage('Test') {
            steps {
                sh "mvn test"
            }
        }

        stage('Test API') {
            steps {
                sh "newmann run mindicador.cl.postman_collection.json"
            }
        }
    }
}
