pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/FranciscoDumont/ing-software-tp2.git', branch: 'master')
        sh '''git clone https://github.com/FranciscoDumont/ing-software-tp2.git
gradle build
'''
      }
    }
  }
}