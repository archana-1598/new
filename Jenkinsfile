pipeline {
     agent {
	     label 'slave'
		 }
	 stages {
	     stage('Compile') {
		     steps {
			       echo "Compiled sucessfully !";
				   }
			}
		 stage('JUnit') {
		    steps {
			       echo "Junit passed successfully!";
				   }
			}
			stage('Qulaity gate') {
		    steps {
			       echo "quality gate passed successfully!";
				   }
			}
			stage('Deploy') {
		    steps {
			       echo "Pass";
				   }
			}
		}
		post {
		   always {
		       echo 'This will always run' 
		    }
			success {
			    echo 'This will run only if failed'
			}
			failure {
			     echo 'This will run only if failed'
			}
			unstable {
			     echo 'This will run only if the run was marked as unstable' 
			}
		}
	}
			
