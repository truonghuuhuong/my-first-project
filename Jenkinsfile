pipeline {
    agent any
    tools {
        jdk 'localJDK'
        maven 'localMaven'
    }
    stages {
        stage('Install') {
            steps {
                sh "mvn clean test"
            }
        }
		stage('Sonar') {
            steps {
                sh "mvn sonar:sonar -Dsonar.host.url=172.17.0.2:9111"
            }
        }
    }
}