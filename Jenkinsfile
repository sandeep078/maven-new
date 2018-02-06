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
   }

}
