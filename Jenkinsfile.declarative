pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building"
            }
        }
        stage('Test') {
            steps {
                echo "Testing"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy"
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