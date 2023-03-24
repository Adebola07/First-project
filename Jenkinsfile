pipeline {
    agent any
    tools {
        maven 'maven'
    }
    environment {
        my_env = credentials ('docker')
        new_env = 'Oyedeji Femi'
    }
    stages {
        stage('testing cred') {
             steps {
                script {
                    sh "echo my name is ${new_env}"
                    sh "echo my creds are ${my_env_USR} and ${my_env_PSW}"
                    def variable = 'zamani'
                    echo "my aka is ${variable}"
                }
            }
        }
        stage ('testing variable'){
            steps {
                script {
                echo "my aka is ${variable}"
                }
            }
        }
       
    }
}