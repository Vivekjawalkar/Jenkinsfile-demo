pipeline {
  agent any 
  stages {
stage('Checkout'){
  steps{
    echo 'Download Code'
  }
}
    stage('Build'){
      steps {
        sh'echo "Hello Jenkins" > output.txt'
        sh 'cat output.txt'
      }
    }
    stage('Test'){
      steps {
        echo 'running testing on a application'
      }
    }
    stage('Archive') {
      steps {
        archiveArtifacts artifacts: 'output.txt'
      }
    }
  }
  post {
    always {
      echo 'Pipeline Finished'
    }
    success {
      echo 'Build Successful'
    }
    failure {
      echo 'Build Failed'
    }
  }
}
