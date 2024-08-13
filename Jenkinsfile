pipeline {
    agent any 
    stages {
        stage ('Build') {
            steps {
                echo "Building the application"
            }
        }
        stage ("DeployToProd") {
            when {
                // this stage should trigger if the branch is stage or production
                expression { BRANCH_NAME ==~ /(production|staging)/}
            }
            steps {
                echo "****** Deploying to Production *******"
            }
        }
    }
}
