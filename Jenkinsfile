pipeline {
  agent none
  stages {
    stage('Pull From Git') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample.git', branch: 'master', credentialsId: 'dfe3b639-920e-45d0-b880-6b7163352b08')
      }
    }
  }
}