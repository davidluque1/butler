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
                       parameters {
  choice choices: ['yes', 'no'], description: '', name: 'cool?'
}
                sh 'echo "Hello, ${PERSON}, nice to meet you"'
                sh label: '', script: 'app.sh'
            }
        }
    }
}
