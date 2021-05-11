pipeline {
     agent any  
	 stages {
	     stage("clone code") {
		     steps {
			     git credentialsId: 'git_credentials', url: 'https://github.com/gabrielf/maven-samples.git'
			}
		}
        stage("build code") {
		    steps {
			   sh "mvn clean install"
			}
		}
	}
}			
