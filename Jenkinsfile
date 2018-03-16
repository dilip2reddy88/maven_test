pipeline {
//agent any
	node ('master'){

	stages{
	   stage('comiling the code '){
		   steps{
		     withMaven(maven :'maven_install')
				{
					sh 'mvn clean compile'
				}
			 
	           }
	}
     }
	}
}
