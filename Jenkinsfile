pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        bat 'echo Hello start'
        git 'https://github.com/DannySe/simple-maven-project-with-tests.git'
        tool 'M3'
      }
    }
    stage('Build') {
      steps {
        bat 'echo middle'
        bat 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }
    stage('Results') {
      steps {
        bat 'echo Done'
      }
    }
  }
}