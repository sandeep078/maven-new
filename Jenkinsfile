pipeline {
  agent any

  stages {
   stage('build') {
      steps {
          sh 'mvn install'
           }
}
     stage('compile step') {
      steps {
          sh 'mvn compile'
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

   }
	post {
	always {
archiveArtifacts artifacts: 'add/target/*.jar', fingerprint: true
archiveArtifacts artifacts: 'sub/target/*.jar', fingerprint: true
}
}


}
