pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'mvn test -Dtest=\!*API*'
      }
    }
    stage('build') {
      steps {
         sh 'mvn -B -DskipTests=true package'
      }
    }
  }
}
