pipeline{
agent any
  stages {
    stage('build'){
      echo "build started"
      sh "docker-compose up"
    }
    stage('test'){
      echo "test started"
      sh 'pa11y-ci'
    }
  }

}
