pipeline {
    agent any 
    environment {
        PATH = "/opt/apache-maven-3.8.1/bin/:$PATH"
    }
    stages {
        stage('fetch code') {
            steps {
                git 'https://github.com/Mamidal/javaloginapp.git'
            }
        }
        stage('SonarQube Analysis') {
            steps {
               	sh "mvn clean verify sonar:sonar -Dsonar.projectKey=test-new"
        }
       }
}
}
