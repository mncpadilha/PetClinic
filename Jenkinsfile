pipeline {
  agent any 

  stages {
    stage("Build (Compiling)") {
      steps {
        sh "mvn install"
      }
    }
    stage("Code Analysis (SonarQube)") {
      steps {
        sh "mvn sonar:sonar -Dsonar.host.url=http://172.17.0.2:9000 -Dsonar.login=910b8ebec527e613c689199d3097e1960ea927c3"
      }
    }
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