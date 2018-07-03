pipeline {
  agent any 

  stages {
    stage("Static Analysis") {
      steps {
        sh "vendor/sonar-runner/bin/sonar-runner"
      }
    }
  }
}