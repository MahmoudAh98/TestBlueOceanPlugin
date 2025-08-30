pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Completed'
        retry(count: 3) {
          sh 'dddvdgcfv'
        }

      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Running Test 2'
          }
        }

        stage('Test 1') {
          steps {
            echo 'Running Test 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy?', ok: 'Yes, i\'am sure')
        echo 'Deployment Completed'
      }
    }

    stage('Notify for new build') {
      steps {
        echo 'New build completed successfuly'
      }
    }

  }
}