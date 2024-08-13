pipeline {
    agent any 
    stages {
        stage ('Build') {
            steps {
                echo "***** Building the application *********"
            }
        }
        stage ('Sonar') {
            steps {
                echo "***** Building the application *********"
            }
        }
        stage ('DockerBuild') {
            steps {
                echo "***** Building the Container application *********"
            }
        }
        stage ('DockerPus') {
            steps {
                echo "***** Pushing  the image *********"
            }
        }
        stage ('DeployToDev') {
            steps {
                echo "***** Deploying  the application to dev env *********"
            }
        }
        stage ('DeployToTest') {
            steps {
                echo "***** Deploying  the application to test env *********"
            }
        }
        stage ('DeployToStage') {
            when {
                branch 'release/*'
            }
            steps {
                echo "***** Deploying  the application to Stage env *********"
            }
        }
        stage ('DeployToProd') {
            when {
                // our application should deploy to prod only if the app is going through TAG
                //vx.x.x ====> v1.2.3
                // v.1.2.3 , it should skip
                tag pattern: "v\\d{1,2}\\.\\d{1,2}\\.\\d{1,2}", comparator: "REGEXP"
            }
            steps {
                echo "***** Deploying  the application to dev env *********"
            }
        }
    }
}
