pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh '''if id -u "jenkins" >/dev/null 2>&1; then
    find / -user jenkins > /tmp/jenkins
else
    echo \'user missing\'
fi'''
      }
    }

  }
}