pipeline {
  agent any
  stages {
    stage('Pull SCM') {
      steps {
        git(url: 'https://github.com/rubsnd/ntsrepo3', branch: 'main', credentialsId: '0e55d9c6-6ca3-4ce5-89aa-04ab3777349d')
      }
    }

    stage('Terraforminit') {
      steps {
        bat(script: 'terraform init', label: 'init')
      }
    }

    stage('Deploy') {
      agent any
      steps {
        bat(script: 'echo "Deploy to Prod"', label: 'Deploy')
      }
    }

  }
}