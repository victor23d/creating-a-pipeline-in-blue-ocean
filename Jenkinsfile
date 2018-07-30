pipeline {
  agent {
    docker {
      image 'alpine'
      args 'ls -l'
    }

  }
  stages {
    stage('stage 123') {
      steps {
        sh 'echo \'hehe\''
      }
    }
    stage('stage 321') {
      parallel {
        stage('stage 321') {
          steps {
            sh 'export ASD=\'aaaaaaa\''
            sh 'echo $ASD'
          }
        }
        stage('') {
          steps {
            echo 'echo $ASD'
          }
        }
      }
    }
  }
}