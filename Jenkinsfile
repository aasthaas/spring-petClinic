pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        // Build the project using Maven
        sh 'mvn clean install'
      }
    }
    
    stage('Test') {
      steps {
        // Run the project's unit tests using Maven
        sh 'mvn test'
      }
    }
    
    stage('Deploy') {
      steps {
        // Deploy the project using Maven
        sh 'mvn deploy'
      }
    }
  }
}
