pipeline {
  agent any

  stages {
    stage ('Build') {
      steps {
        sh 'sudo su'
        sh './gradlew build'
        sh './gradlew test'


      }
    }
  }
}