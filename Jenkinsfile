pipeline {
  agent any
  stages {
      stage ('Build') {
          steps {
              sh 'g++ task5.cpp -o task5'
              echo 'Build Stage successful'
              build job: 'PES1UG20CS130-1'
              
            }
      }
      stage('Test') {
          steps {
              sh './task5' 
              echo 'Test Stage Successful'
          }
      }
      stage ('Deploy') {
          steps {
              echo 'Deployment Successful'
              sh 'exit 1'
          }
      }
    }
    post {
        failure {
            echo 'pipeline failed'
          }
    }
}
      
