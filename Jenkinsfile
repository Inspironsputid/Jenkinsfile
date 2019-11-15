pipeline {
   agent any

   stages {
      stage ('compile stage') {
         steps {
	    withMaven(maven : 'maven_3_0_5') {
	       sh 'mvn clean compile'
	       }
	    }
	}

      stage ('testing stage') {
       steps {
         withMaven(maven : 'maven_3_0_5') {
	       sh 'mvn test'
	       }
	     }
	   }
      stage ('Deployment stage') {
       step {
         withMaven(maven : 'maven_3_0_5') {
	       sh 'mvn deploy'
	       }
	     }
	   }
	 }
	 }
