pipeline {
  agent any
  stages {
    stage('Development Build') {
      steps {
        echo 'Pull source code from SCM repo'
        echo 'Create an build'
      }
    }

    stage('Smoke Test') {
      steps {
        echo 'Run 2 smoke test cases'
      }
    }

    stage('Deploy in QA') {
      steps {
        echo 'Stop the server'
        echo 'Deploy the build in prod'
        echo 'Stop the server'
      }
    }

    stage('Integration Test') {
      parallel {
        stage('Integration Test') {
          steps {
            echo 'Integrating the source code'
          }
        }

        stage('Acceptance Testing') {
          steps {
            echo 'End user testing'
          }
        }

      }
    }

    stage('Certify') {
      steps {
        echo 'Certify the build and handover'
      }
    }

  }
}