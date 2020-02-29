pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        sh 'rsync /var/lib/jenkins/jobs/daw2/ root@192.168.2.36:/var/www/html/'
      }
    }

  }
}