pipeline {
    agent {
        label 'mynode'
    }
    tools {
        maven 'maven'
    }
    environment {
        my_env = credentials ('docker')
        new_env = 'Oyedeji Femi'
    }
    steps {
        step('testing cred'){
            script {
                sh "echo my name is ${new_env}"
                sh "echo my creds are ${my_env_USR} and ${my_env_PWD}"
            }
        }
    }
}