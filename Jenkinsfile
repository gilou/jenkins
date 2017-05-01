node('localnode') {
  stage('Test ansible') {
    sh 'ansible --version'
  }
  stage('Run playbook') {
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
  }
}
