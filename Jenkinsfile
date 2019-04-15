pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "hello, world"'
            }
            input {
                    message "proceed?"
                    ok "yes"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Eric', description: 'name')
                    }
                }
        }

        stage('test') {
            steps {
                echo ${PERSON}
            }
        }
    }
}