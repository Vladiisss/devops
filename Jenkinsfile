pipeline {
    agent any

    environment {
        GO111MODULE = 'on'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
                dir('/workspace') {
                    sh 'go test ./...'
                }
            }
        }

        stage('Build') {
            steps {
                dir('/workspace') {
                    sh 'go build ./...'
                }
            }
        }
    }
}
