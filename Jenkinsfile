pipeline {
  agent {
    kubernetes {
      yamlFile 'build-agent.yaml'
      idleMinutes 1

    }
  }
  stages {
    stage('Run docker') {
      steps {
        container('tools') {
          sh 'scripts/build.sh'
        }
      }
    }
  }
}
