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
		archive 'add/target/*.jar'
}
}


}
