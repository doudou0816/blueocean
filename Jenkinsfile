pipeline {
  agent any
  stages {
    stage('check out code') {
      steps {
        git(url: 'https://github.com/doudou0816/simple-java-maven-app', credentialsId: 'access-token')
      }
    }

    stage('complie code') {
      steps {
        sh 'mvn install package'
      }
    }

    stage('build image') {
      steps {
        sh 'kaniko-excutor -f Dockerfile'
      }
    }

  }
}