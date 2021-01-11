pipeline {
  agent any
  stages {
    stage('build') {
      input {
        message 'proceed?'
        id 'yes'
        parameters {
          string(name: 'PERSON', defaultValue: 'Eric', description: 'name')
        }
      }
      steps {
        sh '''echo "Hello, ${PERSON}, nice to meet you on ${UBUNTU}"
echo "da"'''
        sh 'chmod +x app.sh'
        sh './app.sh'
      }
    }

    stage('archive artifacts') {
      steps {
        archiveArtifacts(artifacts: 'target/*.jar', fingerprint: true)
      }
    }

  }
  parameters {
    choice(name: 'UBUNTU', choices: ['18.10', '19.04'], description: 'Chose Ubuntu Release')
  }
}