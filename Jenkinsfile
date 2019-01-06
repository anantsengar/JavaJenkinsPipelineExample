pipeline {
  agent {
    node {
      label 'Git'
    }

  }
  stages {
    stage('') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample.git', credentialsId: 'dfe3b639-920e-45d0-b880-6b7163352b08', branch: 'master')
      }
    }
  }
}