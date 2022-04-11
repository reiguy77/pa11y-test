pipeline{
    agent any
      stages {
        stage('build'){
        steps{
          echo "build started"
          sh "docker-compose up"
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
