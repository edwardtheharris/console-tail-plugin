#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
node('mvn') {
  stage('checkout') {
    checkout scm
  }
  stage('clean') {

  }
  stage('verify') {
    
  }
  stage('buildPlugin') {
    buildPlugin(platforms: ['linux'])
  }
}
