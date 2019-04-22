pipeline {
  agent any
  stages {
    stage('test1') {
      steps {
        sh 'echo "Test Apurva"'
      }
    }
    stage('test2') {
      parallel {
        stage('test2') {
          steps {
            mail(subject: 'test', body: 'test', from: 'viky@contentsphere.com', to: 'apurva.bhandari@contentserv.com')
          }
        }
        stage('newBranch') {
          steps {
            sh 'echo "Test multibranch"'
          }
        }
      }
    }
  }
}