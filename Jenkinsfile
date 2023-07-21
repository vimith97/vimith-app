pipeline {
  agent {
    label ('slave-1') 
    }
  stages {
    stage ('stage-1') {
           steps {
             sh "sudo docker build -t yogita:1.0"
             sh "sudo docker run -itdp 651:80 --name yogita1 yogita:1.0"
           }
    }
  }
}
