pipeline {
    agent {
	label {
	    label "built-in"
	   }
	}
		 
	stages {
		stage('hello') {
			steps {
                sh "sudo yum install httpd -y"	
                sh "sudo service httpd start"
                sh "sudo cd /var/www/html"
                sh "sudo chmod -R 777 ."
                sh "sudo touch index.html"
                sh "sudo echo 'MY 1st JOB' >> index.html"
                sh "sudo service httpd restart"
                sh "sudo chkconfig httpd on "
			}
		}
	}
}
