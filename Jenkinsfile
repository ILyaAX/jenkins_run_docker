pipeline {
	agent any 
	stages {
		stage ('ssh connect & docker run') {
			steps {
				sh 'scp /var/lib/jenkins/workspace/jenkins_run_docker/docker-compose.yml jenkins@89.208.229.53:/home/jenkins/'
				sh 'ssh jenkins@89.208.229.53'
				sh 'docker-compose up -d'
			}
		}
	}
}