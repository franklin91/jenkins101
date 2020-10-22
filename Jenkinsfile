// Declarative //
pipeline {
  agent any
  triggers {
    cron "H * * * *"
  }
  stages {
  stage('Display IP') {
  steps { 
  echo 'Hello World'
  sh 'curl http://ipinfo.io/ip > my-public-ip.txt'
  }
  }
  post {
   always {
     archiveArtifacts artifacts: 'my-public-ip.txt', followSymlinks: false
      }
  }
}
