node {
  stage('Run playbook') {
    echo "PATH is : ${env.PATH}"
    checkout
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
  }
  stage('Aftermath') {
    sh 'lsb_release -a'
  }
}
