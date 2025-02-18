pipeline {
    agent any
    tools {
      jdk 'Java17'
      maven 'Maven3'
    }
    stages {
      stage("Clean Workspace"){
        steps{
          cleanWs()
        }
    }
    stage("Checkout from SCM"){
      steps {
        git branch: 'main', url: 'https://github.com/kushaggarwal/register-app.git'
    }
    }
    stage("Build Application"){
      steps{
        sh "mvn clean package"
      }
    }
      stage("Test Application"){
        steps {
          sh "mvn test"
        }
      }
          
}
}
