pipeline {
    parameters {
        string (name: 'CHANGE_TICKET', defaultValue: 'CH12345', description: 'Please enter your change ticket')
        booleanParam (name: 'Is SRE Approved ?', defaultValue: true, description: 'Is Approval taken from SRE')
        choice(choices: 'Regular\nHotfix', description: 'What Release is this', name: 'RELEASE')
        password(name: 'myPassword', defaultValue:'', description: 'Enter the password')
        credentials(name: 'mycreds', description:'MyDockerCreds', required: true)
    }
    agent any 
    stages {
        stage ('Deploy To Dev') {
            steps {
                echo "Deployed to dev succesfully!"
            }
        }
        stage ('Deploy to Prod') {
            steps {
                echo "Your change ticket ${params.CHANGE_TICKET} is validate"
                echo "Deploy yo prod"
                echo "This is a ${params.RELEASE}"
                echo "The pasword is ${params.myPassword}"
                echo "Selected Credentilas are ${mycreds}"
            }
        }
    }
}
