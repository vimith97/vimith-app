pipeline {
  agent none
  stages {

    stage ('stage-1') {
      agent any 
      
      steps {
      sh "scp /mnt/Dockerfile ec2-user@172.31.86.242:/mnt/slave-1/workspace/Job-1/"
      }
    }
      stage ('stage-2') {
        agent { label 'slave-1' } 
           steps {
             sh "sudo cd /mnt/"
             sh "sudo docker build -t yogita:1.0 ."
             sh "sudo docker run -itdp 651:80 --name yogita1 yogita:1.0"
           }
    }
             }
        }
