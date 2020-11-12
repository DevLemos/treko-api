pipeline {
  agent {
    docker{
      image "node:8-alpine"
      args "--network=lemos"
    }
  }
  stages {
    stage("Build"){
      steps {
        
        sh "chmod +x ./scripts/dropdb.sh"
        sh "npm install"

      }
    }
    stage ("Test") {
      steps {
        sh "npm run test:ci"
      }
    }
  }
  
}
