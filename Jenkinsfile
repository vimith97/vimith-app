pipeline {
  agent any
  stages {
    stage ('23q1-deploy') {
      steps {
        /*sh "yum install docker -y"
        sh "systemctl start docker"
        sh "systemctl enable docker"
        sh "docker stop vimith"*/
        sh "docker system prune -a -f"
        sh "docker run -itdp 80:80 -v /mnt/vimith15:/usr/local/apache2/htdocs/ --name vimith httpd"
        sh "docker exec vimith chmod -R 777 /usr/local/apache2/"
      }
    }
  }
}
