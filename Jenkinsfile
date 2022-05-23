pipeline {

  agent any

tools {
        gradle "GRADLE_7.4.2"
    }
  stages {
    stage ('Build') {
      steps {

        withGradle{sh 'gradle clean build'}

        archiveArtifacts artifacts: 'build/reports/tests/**/*',
                           allowEmptyArchive: true,
                           fingerprint: true

        publishHTML (target : [allowMissing: false,
         alwaysLinkToLastBuild: true,
         keepAll: true,
         reportDir: 'build/reports/tests/test',
         reportFiles: 'index.html',
         reportName: 'HTML Report',
         reportTitles: 'HTML Report'])





      }


    }
  }
}
