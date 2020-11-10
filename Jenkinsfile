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
            sh 'echo Test'
          }
        }

        stage('Stage3') {
          steps {
            sh 'exit 0'
          }
        }

      }
    }

    stage('NewStage4') {
      parallel {
        stage('NewStage4') {
          steps {
            echo 'Sample'
          }
        }

        stage('NewStater5') {
          steps {
            sh 'echo "This is good"'
          }
        }

      }
    }

    stage('Final Stage') {
      parallel {
        stage('Final Stage') {
          steps {
            echo 'Smaple message'
            echo 'New Message'
          }
        }

        stage('Mark stage') {
          steps {
            echo 'Somthing'
          }
        }

      }
    }

    stage('error') {
      steps {
        echo 'Last step'
        sh '''git status
git log'''
      }
    }

  }
}