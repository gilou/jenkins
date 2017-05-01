pipeline {
	agent { label 'localnode' }
	stages {
		stage('Test ansible') {
			steps {
				sh 'ansible --version'
			}
		}
		stage('Run playbook') {
			steps {
				ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
			}
		}
	}
}
