pipeline {
  agent any

  stages {
    stage ('Build') {
      steps {
        bat '.\gradlew build'

        bat '.\gradlew test'


      }
    }
  }
}