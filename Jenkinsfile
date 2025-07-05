pipeline {
  agent any
  stages {
    stage('clone'){
      steps {
        git 'https://github.com/gladsonm934/app3.git'
      }
    }
    stage('Build Docker Image'){
      steps {
        script {
          dockerImage = docker.build("app3")
        }
      }
    }
    stage('Run Docker Container'){
      steps {
        script {
          dockerImage.run("-d -p 8086:80")
        }
      }
  }  
}
}
