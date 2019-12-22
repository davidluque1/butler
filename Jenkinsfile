pipeline {
    agent any
    parameters {
        choice choices: ['18.10', '19.04'], description: '', name: 'UbuntuRelease?'
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
                sh 'echo "Hello, ${PERSON}, nice to meet you on ${UbuntuRelease}"'
                sh 'chmod +x app.sh'
                sh label: '', script: './app.sh'
            }
        }
    }
}
