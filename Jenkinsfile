pipeline {
    agent {
	label {
	    label "slave-1"
	   }
	}
		 
	stages {
		stage('hello') {
			steps {
                sh "sudo yum install httpd -y"	
                sh "sudo service httpd start"
                sh "sudo cd /var/www/html"
                sh "sudo chmod -R 777 ."
                sh "sudo service httpd restart"
                sh "sudo chkconfig httpd on "
			}
		}
	}
}
