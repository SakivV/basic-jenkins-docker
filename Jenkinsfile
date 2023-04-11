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
                sh 'docker build -t cloudmagicmaster/cloudnation:1.0 .'
            }
        }

        stage('PushImage') {
            steps {
                withCredentials([string(credentialsId: 'dockerpwd', variable: 'dockerpwd')]) {
                  sh 'docker login -u cloudmagicmaster -p ${dockerpwd}'
                  sh 'docker push cloudmagicmaster/cloudnation:1.0'
              }
            }
        }


    }
}
