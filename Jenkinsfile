pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.host.url=http://172.31.27.121:9000 \\
  -Dsonar.login=sqp_6fae2854cd9f8fa14652ad282877978fe4bfc0ab'''
      }
    }

  }
}