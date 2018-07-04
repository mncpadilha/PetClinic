pipeline {
  agent any 

  stages {
    stage("Build (Compiling)") {
      steps {
        sh "mvn install"
      }
    }
    /*stage("Code Analysis (SonarQube)") {
      steps {
        sh ""
      }
    }*/
    stage("Unit Test (JUnit)") {
      steps {
        sh "mvn test"
      }
    }
    stage("Publish (Deploy)") {
      steps {
        sh "mvn clean deploy -Dmaven.test.skip=true"
      }
    }
  }
}