pipeline {
  agent {
    docker {
      label 'scanner'
      args '-v /tmp:/tmp'
      image 'raspberry-sane-git:latest'
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