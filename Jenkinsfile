pipeline {
  agent any
  stages {
    stage ('23q1-deploy') {
      steps {
        sh "yum install docker -y"
        sh "systemctl start docker"
        sh "systemctl enable docker"
        
        sh "docker system prune -a -f"
        sh "docker run -itdp 80:80 --name vimith httpd"
        sh "docker cp index.html vimith:/usr/local/apache2/htdocs"
        sh "docker exec vimith chmod -R 777 /usr/local/apache2/"
      }
    }
  }
}
