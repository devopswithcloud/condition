pipeline {
    agent any 
    environment {
        //DEPLOY_TO = 'production' // just an environment variable 
        DEPLOY_TO = 'somethingelse'
    }
    stages {
        stage ('BuildOnly') {
            steps {
                echo "***** Building the app ******"
            }
        }
        stage ('anyofstage') {
            when { 
                allOf {
                    expression { BRANCH_NAME ==~ /(production|staging)/} // condition 1
                    environment name: 'DEPLOY_TO', value: 'production' // condition 2 
                }

            }
            steps {
                echo "Deploying to k8s cluster"
            }
        }
    }
}
