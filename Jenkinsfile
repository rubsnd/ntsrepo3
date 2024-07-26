pipeline {
    agent any

    stages {
        stage('Stage1') {
            steps {
                git branch: 'main', credentialsId: '0e55d9c6-6ca3-4ce5-89aa-04ab3777349d', url: 'https://github.com/rubsnd/ntsrepo3'
            }
        }
      stage('Stage2') {
            steps {
                bat 'terraform init'
            }
        }
      stage('Stage3') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
