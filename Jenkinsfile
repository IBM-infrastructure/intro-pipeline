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
        sh '''echo "${MY_NAME}, you\'re learning!"

echo "Hello ${params.Name}!"'''
      }
    }
  }
  environment {
    MY_NAME = 'STEVE'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}