node('localnode') {
  stage('Test ansible') {
    try {
      sh 'ansible --version'
    }
    catch (e) {
      echo 'ansible not installed?'
    }
  }
  stage('Run playbook') {
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
  }
}
