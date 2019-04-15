pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "hello, world"'
                sh 'echo "next step"'
            }
        }

        stage('test') {
            steps {
                sh 'echo "test step"'
            }
        }
    }
}