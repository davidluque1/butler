pipeline {
    agent any
    parameters {
        choice choices: ['18.10', '19.04'], description: '', name: 'Ubuntu Release' ?'
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
                sh 'echo "Hello, ${PERSON}, nice to meet you on ${Ubuntu Release}"'
                sh 'chmod +x app.sh'
                sh label: '', script: './app.sh'
            }
        }
    }
}
