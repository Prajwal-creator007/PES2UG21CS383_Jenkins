pipeline {
  agent any
  stages {
    // stage('clone repository') {
    //   steps {
    //     checkout([$class: 'GitSCM',
    //     branches: [[name: '*/main']],
    //     userRemoteConfigs: [[url:
    //   }
    // }
     stage('Build') {
       steps {
        build 'PES2UG21CS383-1'
         bhynjunsh 'g++ main.cpp -o output'
       }
     }
      stage('Test') {
        steps {
          sh './output'
        }
      }
      stage('Deploy') {
        steps {
          echo 'deploy'
        }
      }
  }
      post{
        failure{
          error 'Pipeline failed'
        }
      }
}

