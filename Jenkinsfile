pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample', branch: 'master', credentialsId: 'fd43a5c5998deac7528ade6173c9012fc03b0cde')
      }
    }
    stage('Build Image') {
      steps {
        dockerNode(dockerHost: 'tcp://192.168.2.215:2376/', image: 'anantsengar/dockerapp:1.0.0')
      }
    }
  }
}