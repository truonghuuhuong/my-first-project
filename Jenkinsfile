pipeline {
    agent any
    tools {
        jdk 'jdk8'
        maven 'maven3'
    }
    stages {
        stage('Install') {
            steps {
                sh "mvn clean test"
            }
        }
		stage('Sonar') {
            steps {
                sh "mvn sonar:sonar -Dsonar.host.url=172.17.0.1:9111 -Dsonar.login=6724abe65b800ef674aa2f0114d2bd20e3ab3a5e"
            }
        }
    }
}