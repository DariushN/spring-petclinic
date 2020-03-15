pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh './mvnw compile'
      }
    }

    stage('test') {
      steps {
        sh './mvnw test'
      }
    }

    stage('package') {
      steps {
        sh './mvnw package'
      }
    }
    
    stage('deploy') {
      when {
        branch 'master'
      }
      steps {
        sh './mvnw deploy'
      }
    }
  }
}

