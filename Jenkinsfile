pipeline {
    agent { 
        node {
            label 'docker-agent-python-new'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff..
                '''"
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deploy....'
                sh '''
                echo "deploying software.."
                '''
            }
        }
    }
}
