// When: at least one condition must be specified 
// https://www.jenkins.io/doc/book/pipeline/syntax/#when
// If more than one condition is specified, all condtions must return true for the stage to be executed

pipeline {
    agent any 
    environment {
        //DEPLOY_TO = 'production' // just an environment variable 
        DEPLOY_TO = 'somethingelse'
    }
    stages {
        stage ('WhenStage') {
            when {
                // environment based condition
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo "Deploying to When Stage"
            }
        }
    }
}
