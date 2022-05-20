pipeline {
  agent any

  stages {
    stage ('Build') {
      steps {

      sh './gradlew build'

      }

      post {
              always {

                publishHTML target: [
                    allowMissing: false,
                    alwaysLinkToLastBuild: false,
                    keepAll: true,
                    reportDir: '/var/lib/jenkins/workspace/APITestingPipeline/build/reports/tests/test',
                    reportFiles: 'index.html',
                    reportName: 'HTML Report'
                  ]
              }
            }
    }
  }
}
