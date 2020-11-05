pipeline {
  agent any
  stages {
    stage('clone') {
      steps {
        sh 'git clone https://github.com/codigo-code/devsecops.git '
      }
    }

    stage('deploy') {
      steps {
        sh '''cd  devsecops
docker run -p 8080:8080 -it codigocode-test'''
      }
    }

    stage('Open') {
      steps {
        sh 'start http://localhost:8080/saludar'
      }
    }

  }
}