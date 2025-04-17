pipeline {
  agent any
  stages {
    stage('git scm update') {
      steps {
        git url: 'https://github.com/Doro1126/jenkins.git', branch: 'main'
      }
    }
    stage('test') {
      steps {
        sh '''
        pwd
        echo "hello"
        '''
      }
    }
    stage('test2') {
      steps {
        sh '''
        touch /home/seonho/doro/jenkins-test.txt
        echo "test123" >> /home/seonho/doro/jenkins-test.txt
        cat /home/seonho/doro/jenkins-test.txt
        '''
      }
    }
  }
}
