pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t app:test .'
      }
    }
    stage('Test') {
      steps {
        echo 'Test mejorado '
        sh '/bin/nc  localhost 22'
        sh '/bin/nc  localhost 80'
      }
    }
    stage('Subir al registro de docker') {
      steps {
        echo 'Push al registro de docker'
        sh 'docker tag app:test app:stable'
        sh 'docker push app:test app:stable'
      }
    }

  }
}
