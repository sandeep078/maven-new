pipeline {
  agent any

  stages {
   stage('build') {
      steps {
          sh 'mvn install'
           }
}
     stage('install') {
      steps {
          sh 'mvn install'
            }
}
	options{
		buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1' ))
}

  stage('docker step') {
      steps {
          sh 'sudo docker pull centos'
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
