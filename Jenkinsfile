node {
      stage('========SCM CHECKOUT======='){
      git credentialsId: 'dfe3b639-920e-45d0-b880-6b7163352b08', url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample.git'
      }
      stage('======== MVN PACKAGE========'){
          def mvnHome = tool name: 'maven-3', type: 'maven'
          def mvnCMD = "${mvnHome}/bin/mvn"
          sh '${mvnCMD} clean package'
      }
      stage('========Build Docker Image==========')
      {
          sh 'docker build -t anantsengar/dockerapp:1.0.0'
      }


      withCredentials([string(credentialsId: 'docker-hub-pwd', variable: 'dockerHubPassword')]) {
    // some block
     }

}

pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/anantsengar/JavaJenkinsPipelineExample.git', branch: 'master', credentialsId: 'dfe3b639-920e-45d0-b880-6b7163352b08')
      }
    }
  }
}