pipeline {
	agent any
	stages {
		stage ('ssh connect & docker run') {
			steps {
				sh 'ssh jenkins@89.208.229.53'
				sh 'docker pull 89.208.222.153:8123/webapp'
				sh 'docker run --rm -d -p 80:8080 89.208.222.153:8123/webapp'
			}
		}
	}
}