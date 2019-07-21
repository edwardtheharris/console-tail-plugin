#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
ansiColor() {
  node('mvn') {
    stage('checkout') {
      checkout scm
    }
    stage('clean') {
      withMaven {
        echo(sh(label: 'mvn clean',
                script: 'mvn -e clean',
                returnStdout: true))
      }
    }
    stage('verify') {
      withMaven {
        echo(sh(label: 'mvn verify',
                script: 'mvn -e verify',
                returnStdout: true))
      }
    }
    stage('buildPlugin') {
      buildPlugin(platforms: ['linux'])
    }
  }
}
