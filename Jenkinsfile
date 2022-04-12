pipeline{
    agent any
      stages {
        stage('build'){
        agent {
          sh "docker-compose up -d"
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
