pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sleep 2
        echo 'Hello, Executng  pipeline'
        sh 'echo " This is shell"'
      }
    }

  }
  environment {
    task = 'demo'
    tag = '0.2.4'
  }
}