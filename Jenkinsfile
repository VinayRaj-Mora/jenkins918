pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    environment{
        NAME = "Jenkins"
    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $NAME
                    """
                }
                
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Testing"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                        echo "Deploying"
                    """
                }
            }
        }
    }
    post{
        always{
            echo "This will always run"
            cleanWs()
        }
        success{
            echo "This will run only if successful"
        }
        failure{
            echo "This will run only is failed"
        }
    }
}