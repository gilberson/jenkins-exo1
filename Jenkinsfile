pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh 'grep jenkins /etc/passwd'
      }
    }

    stage('stage2') {
      steps {
        sh '''if test `grep -c jenkins /etc/passwd`-ne 0
then
sudo find / -user jenkins > /tmp/jenkins
fi'''
      }
    }

    stage('stage3') {
      steps {
        sh '''for i in `cat /tmp/jenkins`
do
ls -il $i
done'''
      }
    }

  }
}