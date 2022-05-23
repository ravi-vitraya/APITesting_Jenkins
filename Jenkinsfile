pipeline {

  agent any

tools {
        gradle "GRADLE_7.4.2"
    }
  stages {
    stage ('Build') {
      steps {

        withGradle{sh 'gradle clean build'}






      }
       post {
              always {

                publishHTML target: [
                    allowMissing: false,
                    alwaysLinkToLastBuild: false,
                    keepAll: true,
                             reportDir: 'build/reports/tests/test',
                             reportFiles: 'index.html',
                             reportName: 'HTML Report',
                             reportTitles: 'HTML Report'
                  ]
              }
            }


    }
  }
}
