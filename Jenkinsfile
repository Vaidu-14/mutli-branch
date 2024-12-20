pipeline {
    agent {
	label {
	    label "built-in"
	   }
	}
		 
	stages {
		stage('hello') {
			steps {
                sh "yum install httpd -y"	
                sh "service httpd start"
                sh "cd /var/www/html"
                sh "chmod -R 777 ."
                sh "touch index.html"
                sh "echo 'MY 1st JOB' >> index.html"
                sh "service httpd restart"
                sh "chkconfig httpd on "
			}
		}
	}
}
