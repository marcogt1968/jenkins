pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t app .'
      }
    }
    stage('Test') {
      steps {
        echo 'Test mejorado '
      }
    }
    stage('Deploy') {
      agent any
      steps {
        echo 'Despliegue'
      }
    }

  }
}
