pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh '/bin/nc -vz 192.168.2.36'
        sh '/bin/nc -vz 192.168.2.37'
      }
    }
    stage('Despliegue') {
      steps {
        sh 'rsync -av /var/lib/jenkins/workspace/daw2_master/ root@192.168.2.36:/var/www/html/'
        sh 'rsync -av /var/lib/jenkins/workspace/daw2_master/ root@192.168.2.37:/var/www/html/'
        sh 'ssh root@192.168.2.36 systemctl restart apache2'
        sh 'ssh root@192.168.2.37 systemctl restart nginx'
      }
    }
  }
}
