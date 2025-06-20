pipeline {
    agent any

    tools {
        gradle 'Gradle-7'
        jdk 'jdk-17'
    }

    stages {
        stage('Clone repository') {
            steps {
                echo 'Cloning repository'
                git 'https://github.com/d-0pZ/java-todo.git'
            }
        }
        stage('Build project') {
            steps {
                    sh 'gradle build'
            }
        }
        stage('Tests') {
            steps {
                    sh 'gradle test'
            }
        }
      }   
    }
}
