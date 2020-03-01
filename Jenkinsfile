pipeline {
  agent any
  stages {
    stage('Inicio') {
      steps {
        sh 'rsync -av /var/lib/jenkins/workspace/daw2_master/ root@192.168.2.36:/var/www/html/'
        sh 'rsync -av /var/lib/jenkins/workspace/daw2_master/ root@192.168.2.37:/var/www/html/'
      }
      steps {
        sh 'ssh root@192.168.2.36 systemctl restart apache2'
        sh 'ssh root@192.168.2.37 systemctl restart nginx'
      }
    }
  }
}
