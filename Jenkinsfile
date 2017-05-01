node('localnode') {
  env.PATH = "${env.PATH}:${env.HOME}/.local/bin"
  stage('Test ansible') {
    try {
      sh 'ansible --version'
    }
    catch (e) {
      echo 'ansible not installed?'
      try {
        sh 'pip install --user ansible'
      }
      catch (e2) {
        echo 'pip did not work :('
        throw e2
      }
    }
  }
  stage('Run playbook') {
    ansiblePlaybook installation: 'ansible', limit: 'localhost', playbook: 'update.yml'
  }
}
