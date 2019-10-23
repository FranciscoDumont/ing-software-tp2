pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/FranciscoDumont/ing-software-tp2.git', branch: 'master')
        sh '''git pull
'''
        sh 'gradle build'
        sh './mvnw package'
        sh 'java -jar target/*.jar'
      }
    }
  }
}