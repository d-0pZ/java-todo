pipeline {
    agent any

    tools {
        gradle 'Gradle-7.6'
        jdk 'jdk-17'
    }

    stages {
        stage('Clone repository') {
            steps {
                echo 'Cloning repository'
                git 'https://github.com/d-0pZ/java-todo.git'
            }
        }
        stage('Build') {
            steps {
                withEnv(["JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64",
                "PATH=/usr/lib/jvm/java-17-openjdk-amd64/bin:$PATH"
                ]) {
                    sh 'java -version'
                    sh 'gradle build'
                }
            }
        }
        stage('Tests') {
            steps {
                    sh 'gradle test'
            }
        }
    }   
 }

