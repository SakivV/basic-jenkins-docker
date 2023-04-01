pipeline {
    agent any
    stages {
        stage('VerifyBranch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('VerifyDocker') {
            steps {
                sh 'docker -v'
            }
        }
        stage('HelloDocker') {
            steps {
                sh 'sudo docker run hello-world'
            }
        }
    }
}
