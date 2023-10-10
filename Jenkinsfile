pipeline {
	agent any
	
	tools {
		jdk "Java-11.0.20.1"
		maven "Maven-3.6.3"
	}
	stages {
	   stage ('Compile Stage') {

		steps {
		   
  		   withMaven(maven : 'Maven-3.6.3') {
			bat 'mvn clean compile'
		    }
		}
	    }

	    stage ('Testing stage') {
		
		steps {

		   withMaven(maven : 'Maven-3.6.3') {
			bat 'mvn test'
		   }
		}
	     }

	     stage ('Packaging Stage') {

		steps {

		   withMaven(maven : 'Maven-3.6.3') {
			bat 'mvn package'
		   }
		}
	      }
	   }
}
