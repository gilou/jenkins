#!groovy
node {
  stage('Checkout repository') {
    checkout scm
  }
  stage('Run playbook') {
    echo "PATH is : ${env.PATH}"
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: "${env.PLAYBOOK}"
  }
  stage('Aftermath') {
    sh 'lsb_release -a'
  }
}
