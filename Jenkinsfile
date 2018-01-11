pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.test-armv7'
      label 'scanner'
      args '-v /tmp:/tmp'
    }
  }
  stages {
    stage('Test') {
      steps {
        sh 'tox -- --with-scanner'
      }
    }
  }
}
