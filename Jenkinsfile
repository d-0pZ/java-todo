pipeline {
  agent any
  stages {
    stage('Find Java Path') {
      steps {
        sh 'which java'
        sh 'readlink -f $(which java)'
        sh 'echo $JAVA_HOME'
      }
    }
  }
}
