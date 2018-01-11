pipeline {
  agent {
    docker {
      image 'phenomique/raspberry-sane-git'
      label 'scanner'
      args '-v /tmp:/tmp'
    }
  }
  stages {
    stage('Test') {
      steps {
        sh 'pip install tox'
        sh 'tox -- --with-scanner'
      }
    }
  }
}
