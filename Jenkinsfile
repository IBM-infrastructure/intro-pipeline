pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello World!'
        sh '''java -version
echo "${TEST_USER_USR}"
echo "${TEST_USER_PSW}"'''
      }
    }
    stage('Say Something') {
      steps {
        echo 'Something'
      }
    }
    stage('Say Name') {
      steps {
        sh 'echo "${MY_NAME}, you\'re learning!"'
      }
    }
  }
  environment {
    MY_NAME = 'STEVE'
    TEST_USER = credentials('test-user')
  }
}