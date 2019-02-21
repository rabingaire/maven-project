pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'clean package'
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts '**/*.war'
      }
    }
  }
}