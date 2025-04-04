pipeline {
  agent any
  stages {
    stage('Clean Up') {
      steps {
        removeDir()
      }
    }

    stage('Checkout'){
      steps {
        git 'https://github.com/Hydrowind/jenkins-maven.git'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Deploy') {
      steps {
        echo 'deploying application...'
      }
    }
  }
}