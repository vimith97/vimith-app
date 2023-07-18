pipeline {
  agent any
  stages {
    stage ('23q2-deploy') {
      steps {
        sh "yum install docker -y"
        sh "systemctl start docker"
        sh "systemctl enable docker"
        sh "docker stop vimith-2"
        sh "docker system prune -a -f"
        sh "docker run -itdp 8081:80 --name vimith-2 httpd"
        sh "docker cp index.html vimith-2:/usr/local/apache2/htdocs"
        sh "docker exec vimith-2 chmod -R 777 /usr/local/apache2/"
      }
    }
  }
}
