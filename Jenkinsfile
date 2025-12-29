pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git 'https://github.com/yourname/yourrepo.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        sh 'docker build -t cicd-demo .'
      }
    }

    stage('Run Container') {
      steps {
        sh 'docker run -d -p 3000:3000 cicd-demo'
      }
    }
  }
}
