pipeline {
    agent any
    stages {
        stage('build') {
            input {
                    message "proceed?"
                    ok "yes"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Eric', description: 'name')
                    }
                }
            steps {
                sh 'echo "Hello, ${PERSON}, nice to meet you"'
            }
        }
    }
}