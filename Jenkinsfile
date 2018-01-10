pipeline {
  agent {
    docker {
      image 'raspberry-sane-git'
      label 'scanner'
      args  '-v /tmp:/tmp'
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
