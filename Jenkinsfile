pipeline {
    agent any
    parameters {
        choice choices: ['yes', 'no'], description: '', name: 'cool?'
    }
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
                sh label: '', script: 'app.sh'
            }
        }
    }
}
