pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        withMaven(maven: 'maven') {
          sh 'mvn clean package '
        }

      }
    }
    stage('archive') {
      steps {
        archiveArtifacts '**/*.war'
      }
    }
    stage('deploy') {
      steps {
        build 'deploy-to-tomcat'
      }
    }
  }
}