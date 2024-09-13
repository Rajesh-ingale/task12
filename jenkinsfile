pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('java') {
            steps {
                git branch: 'main', url: 'https://github.com/dayanandgowda222/java.git'
                bat '''javac demo.java
                  java demo'''
            }
        }
        stage('maven') {
            steps {
               git url: 'https://github.com/dayanandgowda222/mavenproject.git'
               bat 'mvn clean test'
            }
        }
    }
}
