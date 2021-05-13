pipeline {
     agent none
	 stages {
	     stage('Non-parallel stage') {
		     agent {
			          label 'master'
					}
			 steps {
			        echo "This stage will be executed first"
					}
			}
           stage('Run tests') {
		       parallel {
			        stage('Test on slave') {
					    agent {
						     label 'slave'
						}
						steps {
						   echo "Task running on agent"
						}
					}
					stage('Test on master') {
					    agent {
						    label 'master'
						}
						steps {
						    echo "Task1 on master"
						}
					}
				}
			}
		}
	}	
