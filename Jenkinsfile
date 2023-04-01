pipeline {
    agent any
    stages {
        stage('VerifyBranch') {
            steps {
                git branch: "${env.BRANCH_NAME}", url: "${env.REPO_URL}"
            }
        }
    }
}
