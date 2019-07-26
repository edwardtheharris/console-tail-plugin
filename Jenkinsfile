#!/usr/bin/env groovy

/* `buildPlugin` step provided by: https://github.com/jenkins-infra/pipeline-library */
ansiColor() {
  node('mvn') {
    stage('checkout') {
      checkout scm
    }
    // stage('build') {
    //   withMaven {
    //     echo(sh(label: 'mvn clean',
    //             script: 'mvn -e clean verify',
    //             returnStdout: true))
    //   }
    // }
		// stage('artifacts') {
		// 	archiveArtifacts('pom.xml')
		// }
    // stage('buildPlugin') {
    //   buildPlugin(platforms: ['linux'])
    // }
  }
}
