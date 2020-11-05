pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t codigocode-test .'
      }
    }

    stage('deploy') {
      steps {
        sh 'docker run -p 8080:8080 -it codigocode-test'
      }
    }

    stage('') {
      steps {
        sh 'start http://localhost:8080/saludar'
      }
    }

  }
}