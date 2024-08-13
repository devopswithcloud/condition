pipeline {
    agent any 
    parameters {
        string(name: 'PERSON', defaultValue: 'Siva', description: 'Enter Your name')
    }
    stages {
        stage ('ParametersExample') {
            steps {
                echo "Welcome ${params.PERSON}" //${params.key}
            }
        }
    }
}
