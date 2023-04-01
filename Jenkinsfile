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
                sh 'docker run hello-world'
            }
        }
    }
}
