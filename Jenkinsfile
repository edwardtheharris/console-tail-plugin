#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
ansiColor() {
  node('mvn') {
    stage('checkout') {
      checkout scm
    }
    stage('clean') {
      readMavenPom(file: 'pom.xml')
      withMaven('mvn') {
        echo(sh(label: 'mvn clean',
                script: 'mvn clean',
                returnStdout: true))
      }
    }
    stage('verify') {
      withMaven('mvn') {
        echo(sh(label: 'mvn verify',
                script: 'mvn verify',
                returnStdout: true))
      }
    }
    stage('buildPlugin') {
      buildPlugin(platforms: ['linux'])
    }
  }
}
