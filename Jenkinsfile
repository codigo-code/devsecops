pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t codigocode-test .'
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            sh 'echo LOG = sh(docker run codigocode-test)'
          }
        }

        stage('Guardar Log') {
          steps {
            writeFile(file: 'log.txt', text: '${LOG}')
          }
        }

      }
    }

  }
}