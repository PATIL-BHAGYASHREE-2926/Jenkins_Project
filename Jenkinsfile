pipeline {
  agent any
  stages {
    stage('Build') { steps {echo 'Building the project' } }
    stage('Test') { stapes {echo 'Running tests' } }
  }
  post {
    success { echo 'Pipeline succeeded' }
  }
}
