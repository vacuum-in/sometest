pipeline {
  agent any
  stages {
    stage('get git') {
      steps {
        git(url: 'https://github.com/vacuum-in/test1', branch: 'master')
      }
    }
    stage('build') {
      steps {
        build '1'
      }
    }
  }
}