pipeline {
  agent any
  stages {
    stage('TestStage1') {
      parallel {
        stage('TestStage1') {
          steps {
            echo 'This is task1'
            echo 'This is task 2'
          }
        }

        stage('Stage2') {
          steps {
            sh 'exit 121'
          }
        }
        
         stage('Stage3') {
          steps {
            sh 'exit 0'
          }
        }

      }
    }

  }
}
