pipeline {
	agent any 
	triggers {
  pollSCM '*/2 * * * *'
}	
	parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/shubhangi/Documents/DevopsSoftware/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/project1.war /home/shubhangi/Documents/DevopsSoftware/apache-tomcat-9.0.82/webapps'
			}}	
}}
