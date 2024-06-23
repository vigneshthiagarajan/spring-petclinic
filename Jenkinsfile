#!groovy

pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.9.0'
        }
      }
      steps {
        sh 'mvn clean install'
        sh 'docker build -t vigneshthiagarajan/spring-petclinic:latest .'
      }
    }
    // stage('Docker Build') {
    //   agent any
    //   steps {
    //     sh 'docker build -t vigneshthiagarajan/spring-petclinic:latest .'
    //   }
    // }
  }
}