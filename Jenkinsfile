pipeline {
    agent any
    tools{
        maven 'maven_3.9.9'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn compile'

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mvn clean test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'mvn package -DskipTests'
            }
        }
    }
}