pipeline {
    agent any
    stages {
        stage ('Testing') {
            steps {
                echo 'Testing.....'
            }
        }
        stage ('Sonar'){
            steps {
                echo 'Sonar....'
            }
        }
        stage ('publish') {
            steps {
                echo 'publishing...'
            }
        }
        stage ('deploy to dev') {
            when {
    expression {
      env.BRANCH_NAME == 'develop'
      }
  }
            steps {
                echo 'deploying to dev environment..'
            }
        }
        stage ('deploy to prod') {
            when {
    expression {
      env.BRANCH_NAME == 'main'
      }
  }
            steps {
                echo 'deploy to prod......'
            }
        }

    }
}