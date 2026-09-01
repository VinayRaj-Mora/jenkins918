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
                        env
                    """
                }
                
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                        echo "Testing"
                        echo $NAME
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                        echo "Deploying"
                        echo $NAME
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