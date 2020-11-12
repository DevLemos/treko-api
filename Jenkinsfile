pipeline {
  agent {
    docker{
      image "node:8-alpine"
    }
  }
  stages {
    stage("Build"){
      steps {
        
        sh "chmod +x ./scripts/dropdb.sh"
        sh "npm install"
        sh "npx mocha"
      }
    }
    stage ("Test") {
      steps {
        sh "npm run test:ci"
      }
    }
  }
  
}
