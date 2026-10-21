pipeline {
  agent any
  environment { APP_NAME = 'test' }
  stages {
    stage('Checkout') {steps { checkout scm } }
    stage('Build')    {steps { bat 'echo Building' } }
    stage('Test')     {steps { bat 'echo Running tests' } }
  }
  post {
    success {echo 'All stages passes' }
    failure { echo 'Something failed' }
  }
}
