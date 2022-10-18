pipeline {
  agent any
  stages {
  stage('SSH into the server') {
    steps {
        script {
            def remote = [:]
            remote.name = 'docker1'
            remote.host = 'docker1.do1.lab'
            remote.user = 'jenkins'
            remote.password = 'admin'
            remote.allowAnyHosts = true
        }
    }
}
    
    stage('Docker Compose Config') {
      steps {
    
        sh 'docker compose config '
        
      }
    }
    stage('Docker Compose Build') {
      steps {
       
        sh 'docker compose build'
        
      }
    }
    stage('Docker Compose Up') {
      steps {
        
        sh 'docker compose up -d'
        
      }
    }
  }
}  
