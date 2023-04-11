pipeline {
    agent any
    stages {
        stage('VerifyBranch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('VerifyDockerVersion') {
            steps {
                sh 'docker -v'
            }
        }
        stage('TestDocker') {
            steps {
                sh 'docker run hello-world'
            }
        }
        stage('BuildDocker') {
            steps {
                sh 'docker build -t nginx-jbuild:1.0 .'
            }
        }
    }
}
