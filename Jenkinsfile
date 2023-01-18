pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
        retry(count: 3) {
          sh 'date'
        }

      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test Stages') {
          steps {
            echo 'Test Stages is starting'
            sh 'date'
          }
        }

        stage('Test1') {
          steps {
            echo 'test1 is starting'
            sh 'date'
          }
        }

        stage('Test2') {
          steps {
            echo 'test2 is starting'
            sh 'date'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'are you sure to deploy?', ok: 'yes, iam sure')
        echo 'deployment completed'
      }
    }

    stage('notify new build') {
      steps {
        echo 'notify new build'
      }
    }

  }
}