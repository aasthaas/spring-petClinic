pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        // Build the project using Maven
        sh './mvnw clean install -P buildDocker'
      }
    }
    
    stage('List files') {
      steps {
        // Run the project's unit tests using Maven
        sh 'ls -al'
      }
    }
  }
}
