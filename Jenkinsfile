pipeline {
    agent any
    stages {
        stage('Initialize'){
        def dockerHome = tool 'docker-install'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage('create Docker image') {
            steps {
                echo "building docker image version ${VERSION} ..."
                sh 'sudo docker build -t hello-jenkinspipelines:$VERSION .'
            }
        }
    }
}
