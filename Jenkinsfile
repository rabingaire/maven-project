pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('archive') {
      steps {
        archiveArtifacts '**/*.war'
      }
    }
  }
}