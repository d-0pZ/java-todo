pipeline {
  agent any
  tools {
    jdk 'jdk-17'     
    gradle 'Gradle-7.6'
  }
  stages {
    stage('Clone repository') {
      steps {
        git 'https://github.com/d-0pZ/java-todo.git'
      }
    }
    stage('Build') {
      steps {
        sh 'java -version'
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
