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
        sh 'apt-get install python3-pip'
        sh 'pip install tox'
        sh 'tox -- --with-scanner'
      }
    }
  }
}
