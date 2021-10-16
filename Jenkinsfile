pipeline {
	agent {
		any {
		registryCredentialsId '642e0ecf-859e-4a08-bc5a-c56e1cc89ac8'
		registryUrl 'http://89.208.222.153:8123'
		}
	}
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