pipeline {
    agent any
    stages {
      stage('Initialize'){
        def dockerHome = tool 'docker-install'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage('Build image') {
            steps {
                echo 'Starting to build docker image'

                script {
                    def customImage = docker.build("my-image:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
}