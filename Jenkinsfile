node('localnode') {
  stage('Test ansible') {
      sh 'ansible --version'
  }

  stage('Run playbook') {
    echo "PATH is : ${env.PATH}"
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
  }
}
