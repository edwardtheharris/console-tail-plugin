#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
node('mvn') {
  stage('checkout') {
    checkout scm
  }
  stage('buildPlugin') {
    buildPlugin(platforms: ['linux'])
  }
}
