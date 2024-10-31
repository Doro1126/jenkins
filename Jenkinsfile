pipeline {
  agent any
  stages {
    stage('git scm update') {
      steps {
        git url: 'https://github.com/Doro1126/jenkins.git', branch: 'main'
      }
    }
    stage('docker build and push') {
      steps {
        sh '''
        sudo docker build -t doro0704/keduit:purple .
        sudo docker push doro0704/keduit:purple
        '''
      }
    }
    stage('deploy and service') {
      steps {
        sh '''
        sudo kubectl apply -f jenkins.yml
        '''
      }
    }
  }
}
