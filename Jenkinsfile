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
                    sh 'echo my creds are $my_env_USR and $my_env_PSW'
                    env.variable = 'zamani'
                    sh 'echo testing...'
                    
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
        stage ('ssh') {
            steps {
                script {
                    sshagent(['nodes_job']) {
                         sh "ssh -o StrictHostKeyChecking=no ubuntu@54.196.184.145 ls -al"
                    }
                }
            }
        }
    }
}