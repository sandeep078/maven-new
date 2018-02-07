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
         stage('install stage') {
      steps {
          sh 'mvn package'
           }
}
  stage('docker step') {
      steps {
          sh 'docker pull centos'
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
