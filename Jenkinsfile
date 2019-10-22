pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/FranciscoDumont/ing-software-tp2.git', branch: 'master')
        sh '''git pull
'''
        sh 'gradle build'
        sh 'java -jar build/libs/spring-petclinic-2.2.0.BUILD-SNAPSHOT.jar'
      }
    }
  }
}