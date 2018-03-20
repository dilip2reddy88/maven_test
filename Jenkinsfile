pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
       //def mvnHome = tool 'maven_install'
        bat(/"maven_install\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
    }
    stage('archive and Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archive 'target/*.jar'
      }
    }
  }
}
