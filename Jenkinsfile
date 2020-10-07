pipeline {
  agent any
  stages {
    stage('Build ') {
      steps {
        echo 'Build Completed'
        retry(count: 3) {
          sh 'ccc'
        }

      }
    }

    stage('Test1') {
      parallel {
        stage('Test1') {
          steps {
            echo 'Running Test1'
          }
        }

        stage('Test2') {
          steps {
            echo 'Running Test2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to deploy ?', ok: 'YES iam sure ')
        echo 'Deploy Completed'
      }
    }

    stage('Notify for new Build ') {
      steps {
        echo 'New build Completed successfuly '
      }
    }

  }
}