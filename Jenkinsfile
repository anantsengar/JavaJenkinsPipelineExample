pipeline {
  agent {
    node {
      label 'SCM CHECKOUT'
    }

  }
  stages {
    stage('SCM CHECKOUT') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample.git', branch: 'master', credentialsId: 'dfe3b639-920e-45d0-b880-6b7163352b08')
      }
    }
  }
}