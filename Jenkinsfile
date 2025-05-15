pipeline {
    agent {
        node {
            label 'docker-agent-python-new'
        }
    }
    triggers {
        pollSCM('*/3 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                cd myapp
                pip install -r requirement.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 hello world.py
                python3 hello.py --name=Brad
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy....'
                sh '''
                    echo "deploying software.."
                '''
            }
        }
    }
}

