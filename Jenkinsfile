pipeline {
  agent any 

  stages {
    stage("Code Analysis (SonarQube)") {
      steps {
        sh "vendor/sonar-runner/bin/sonar-runner"
      }
    }
    stage("Unit Test (JUnit)") {
      steps {
        sh "vendor/sonar-runner/bin/sonar-runner"
      }
    }
    stage("Build (Compiling)") {
      steps {
        sh "vendor/sonar-runner/bin/sonar-runner"
      }
    }
    stage("Publish (Deploy)") {
      steps {
        sh "vendor/sonar-runner/bin/sonar-runner"
      }
    }
  }
}