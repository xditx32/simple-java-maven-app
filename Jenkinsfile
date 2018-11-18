pipeline {
    agent any
    tools {
        maven 'maven'
        
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
            steps {
                sh 'file 39'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
