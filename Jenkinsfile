pipeline {
  agent any

  stages {
   stage('build') {
      steps {
          sh 'mvn install'
           }
}
     stage('clean') {
      steps {
          sh 'mvn clean'
            }
}
  stage('docker step') {
      steps {
          sh 'sudo docker pull centos'
           }
}
  stage('container step') {
      steps {
          sh 'sudo docker run --name sandy centos -itd /bin/bash'
           }
}



   }
	post {
	always {
archiveArtifacts artifacts: 'add/target/*.jar', fingerprint: true
archiveArtifacts artifacts: 'sub/target/*.jar', fingerprint: true
}
}


}
