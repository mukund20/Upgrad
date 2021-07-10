pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn \'clean install -DskipTests\''
      }
    }

    stage('Unit Test') {
      steps {
        sh 'mvn \'test\''
      }
    }

    stage('Integration Test') {
      steps {
        sh 'mvn \'verify -DskipUnitTests -Parq-wildfly-swarm \''
      }
    }

  }
  environment {
    task = 'demo'
    tag = '0.2.4'
  }
}