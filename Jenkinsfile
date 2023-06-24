pipeline {
  agent any
  tools {
    maven 'maven-3.6.3' 
  }
  stages {
    stage('Checkout') {
      steps {
        git branch: 'master', url: 'https://github.com/aasthaas/spring-petClinic.git'
		}
    }
    stage ('Build') {
      steps {
        sh 'mvn clean install -DskipTests'
      }
    }
	stage ('Test') {
      steps {
        sh 'mvn clean test'
      }
    }
    stage ('Deploy') {
      steps {
        sh '''
            sudo docker system prune -a --volumes -f
            sudo docker compose up -d --no-color --wait
			sudo docker compose ps
        '''
      }
    }
  }
}
