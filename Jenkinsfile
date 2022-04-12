pipeline{
    agent any
    checkout scm
      stages {
        stage('build'){
        agent {
          dockerfile {
              filename 'Dockerfile'
              dir 'server'
              args '-v /tmp:/tmp'
          }
        }
        steps{
          echo "build started"
          }
        }
        stage('test'){
          steps{
          echo "test started"
          sh 'pa11y-ci'
          }
        }
      }
      post {
        always {
            echo 'I will always say Hello again!'
        }
        }

}
