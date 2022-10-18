pipeline{ 
  agent any
  stages {
  stage('SSH into the server and Up Compose') {
    steps {
        script {
            def remote = [:]
            remote.name = 'docker1'
            remote.host = 'docker1.do1.lab'
            remote.user = 'jenkins'
            remote.password = 'admin'
            remote.allowAnyHosts = true
          sshCommand remote: remote, command: "docker compose up"
                }
            }
        }
    }
}
