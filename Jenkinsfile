pipeline {
    agent any
    parameters { choice(name: 'ENVIRONMENT',
                        choices: ['dev', 'staging', 'production']) }
    stages {
        stage('Checkout') { steps { checkout scm } }
        stage ('Quality') { parallel {
            stage('Build') { steps { bat 'echo Build' } }
            stage('Lint') { steps { bat 'echo Lint' } } } }
        stage('Test') { steps { bat 'echo Test' } }
        state('Package') { steps { bat 'echo Package' } }
    }
}
