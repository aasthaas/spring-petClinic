pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        // Build the project using Maven
        sh 'docker --version'
        sh 'java --version'
        sh 'echo $JAVA_HOME'
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
