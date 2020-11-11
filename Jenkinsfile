pipeline {
  agent {
    docker{
      image "node:8-alpine"
    }
  }
  stage {
    stage("Build"){
      steps {
        sh "npm install"
      }
    }
  }
  
}
