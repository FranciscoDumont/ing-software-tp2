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
      }
    }
    stage('Test') {
      steps {
        sh 'gradle test'
      }
    }
    stage('Validate') {
      steps {
        sh 'echo hola'
      }
    }
    stage('Deploy') {
      steps {
        sh 'java -jar target/*.jar'
      }
    }
  }
}