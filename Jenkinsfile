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
        script {
          stage('SSH transfer') {
            script {
              sshPublisher(
                continueOnError: false,
                publishers: [
                  sshPublisherDesc(
                    configName: "testsrv",
                    verbose: true,
                    transfers: [
                      sshTransfer(
                        sourceFiles: "**/one.php"
                      )
                    ])
                  ])
                }
              }
            }

          }
        }
      }
    }