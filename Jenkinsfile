pipeline {
  agent any
  stages {
    stage('get git') {
      steps {
        git(url: 'https://github.com/vacuum-in/sometest', branch: 'master')
      }
    }
  }
}