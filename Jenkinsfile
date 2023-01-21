#!groovy

pipeline {
	agent none
    stage('Docker Build') {
    	agent any
       steps {
      	sh 'docker build -t ${BUILD_NUMBER} .'
      }
    }
  }