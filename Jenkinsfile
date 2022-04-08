pipeline {
  agent any
  stages {
    stage('check out code') {
      steps {
        git 'https://github.com/doudou0816/simple-java-maven-app'
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