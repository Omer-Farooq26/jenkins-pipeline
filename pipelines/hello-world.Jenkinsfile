pipeline {
  agent { docker { image 'node:18-alpine' } }  // LTS, lightweight

  options { timestamps() }

  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Print versions') {
      steps {
        sh 'node --version'
        sh 'npm --version'
      }
    }
    stage('Hello') {
      steps { sh 'echo "✅ Hello from Jenkins in Docker (Node 18)!"' }
    }
  }

  post {
    always { echo "Build finished: ${currentBuild.currentResult}" }
  }
}

