pipeline {
    agent any
    tools {
        jdk 'JDK17'
    }
    environment {
        JAVA_HOME = 'C:/Program Files/Java/jdk-17'
    }
    stages {
        stage('Initialize') {
            steps {
                git branch: 'main', url: 'https://github.com/MedAliGouiaa/JenkinsTest.git'
            }
        }
        stage('Testing Stage') {
            steps {
                withMaven(maven: 'Maven_399') {
                    bat 'mvn test'
                }
            }
        }
        stage('Install Stage') {
            steps {
                withMaven(maven: 'Maven_399') {
                    bat 'mvn install'
                }
            }
        }
    }
}
