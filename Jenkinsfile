pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o newfile newfile.cpp'
        build job: 'PES1UG20CS900-1'
      }
    }
    stage('Test') {
      steps {
        sh './newfile123'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployment Successful'
      }
    }
  }
  
  post {
    failure {
        echo 'Pipeline failed'
    }
  }
}
