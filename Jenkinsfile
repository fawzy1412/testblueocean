pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test Stages') {
          steps {
            echo 'Test Stages is starting'
          }
        }

        stage('Test1') {
          steps {
            echo 'test1 is starting'
          }
        }

        stage('Test2') {
          steps {
            echo 'test2 is starting'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deployment completed'
      }
    }

  }
}