pipeline {
  agent any
  stages {
    stage('enter the build') {
      steps {
        sh 'cd devsecops_master'
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