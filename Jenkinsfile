pipeline{
    agent any

    stages{
        stage('Checkout'){
          steps{
              checkout scm
            }
          }
        stage('Build Image'){
          steps{
              '''
                sh "docker build -t jenkins-mini ."
              '''
            }
          }
        stage('Execute Container'){
          steps{
              '''
                sh "docker run --rm jenkins-mini"
              '''
            }
          }
      }
  }
