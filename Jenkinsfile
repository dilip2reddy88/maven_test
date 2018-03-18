pipeline{
agent any
   stages{
   stage('Build') {
      // Run the maven build
	  def mvnHome = tool 'maven_install'
      bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
   }
   stage('Results') {
      junit '**/target/*.xml'
      archive 'target/*.jar'
   }
   }
}
