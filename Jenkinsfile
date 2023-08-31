pipeline {
    agent any
    stages{
        stage('hello world'){
            steps{
                echo 'Hello World'
            }
        }
        stage('runing pwershell command'){
        steps{
        bat 'dir'
            }
        }
        stage('adding git checkout'){
        when{
        expression{
        env.BRANCH_NAME == 'sample'
        }
        }
        steps{
           git branch: 'sample', credentialsId: 'capstone', url: 'https://github.com/aiqbal8520/capstone-project.git'
        }
        }
    }
}