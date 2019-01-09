pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample', branch: 'master', credentialsId: 'fd43a5c5998deac7528ade6173c9012fc03b0cde')
      }
    }


    stage('DockerBuild') {
      steps {
        dockerNode(dockerHost: 'tcp://localhost:1234', image: 'hello-world')
        {
          withMaven {
            sh 'echo $DOCKER_HOST'
          }
        }
      }
  }
}
}
