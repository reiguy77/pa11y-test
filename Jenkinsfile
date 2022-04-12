pipeline{
    agent any
      stages {
        stage('build'){
        steps{
          sh "docker-compose up -d"
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
