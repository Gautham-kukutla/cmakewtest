pipeline {
	agent any

  stages {
	  stage('Building andn gtesting'){
		  steps{
	    
	cmakeBuild buildDir: 'build', installation: 'InSearchPath', steps: [[withCmake: true]]
	
		   }  }
	  stage('Cppcheck'){
		  steps{
			  publishCppcheck allowNoReport: true, pattern: 'cppcheck-result.xml'
		  }}
  }}
