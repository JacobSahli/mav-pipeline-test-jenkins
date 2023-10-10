pipeline {
	agent any
	
	tools {
		maven "Apache Maven 3.6.3"
	}
	stages {
	   stage ('Compile Stage') {

		steps {
		   
  		   withMaven(maven : 'Apache Maven 3.6.3') {
			bat 'mvn clean compile'
		    }
		}
	    }

	    stage ('Testing stage') {
		
		steps {

		   withMaven(maven : 'Apache Maven 3.6.3') {
			bat 'mvn test'
		   }
		}
	     }

	     stage ('Packaging Stage') {

		steps {

		   withMaven(maven : 'Apache Maven 3.6.3') {
			bat 'mvn package'
		   }
		}
	      }
	   }
}
