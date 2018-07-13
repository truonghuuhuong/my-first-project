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
    }
}