pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -o program_exec hello.cpp'
            }
        }
        stage('Test'){
            steps{
                sh './program_exec'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployment Successful'
            }
        }

    }
    post{
        failure{
            echo 'Pipeline Failed'
        }
    }
}
