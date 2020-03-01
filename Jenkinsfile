pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        sh 'rsync /var/lib/jenkins/workspace/daw2_master/ root@192.168.2.36:/var/www/html/'
      }
    }

  }
}
