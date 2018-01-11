pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.jenkins-armv7'
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
