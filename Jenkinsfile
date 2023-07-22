pipeline {
  agent any
  stages {
    stage ('23q2-deploy') {
      steps {
        sh /*"yum install docker -y"
        sh "systemctl start docker"
        sh "systemctl enable docker"*/
        sh "docker stop vimith-1"
        sh "docker system prune -a -f"
        sh "docker run -itdp 90:80 --name vimith-1 httpd"
        sh "docker cp index.html vimith-1:/usr/local/apache2/htdocs"
        sh "docker exec vimith-1 chmod -R 777 /usr/local/apache2/"
      }
    }
  }
}
