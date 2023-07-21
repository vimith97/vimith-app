pipeline {
  agent {
    label ('slave-1') 
    }
  stages {
    stage ('stage-1') {
           steps {
             sh "scp /mnt/Dockerfile ec2-user@34.226.143.170:/mnt/slave-1/workspace/Job-1/"
             sh "sudo cd /mnt/"
             sh "sudo docker build -t yogita:1.0 ."
             sh "sudo docker run -itdp 651:80 --name yogita1 yogita:1.0"
           }
    }
  }
}

