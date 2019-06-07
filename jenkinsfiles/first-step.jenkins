#!groovy
//Only one build can run
properties([disableConcurentBuilds()])

pipeline {
  agent {
    label 'master'
  }
  options {
    buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
    timestamps()
  }
  stages {
    stage("test") {
      steps {
        sh 'echo $USER'
        echo 'build finished'
      }
    }
  }
}
