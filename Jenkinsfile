pipeline {
  agent any
  stages {
    stage('Hello') {
      parallel {
        stage('Hello') {
          steps {
            echo 'Hello World'
          }
        }

        stage('step2') {
          steps {
            echo 'pipeline2'
          }
        }

      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building'
          }
        }

        stage('step3') {
          steps {
            sleep 10
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Release') {
      parallel {
        stage('Release') {
          steps {
            echo 'Releasing'
          }
        }

        stage('gradle') {
          steps {
            sleep 5
          }
        }

      }
    }

  }
}