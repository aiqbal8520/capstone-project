pipeline {
    agent any
    parameters{
    choice(name:'Branch_Name',choices:['master','sample'],description:'giving the branch choice')
    string(name:'user name', defaultvalues:'yusha', description:'asking the user name')
    }
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
           git branch: '$Branch_Name', credentialsId: 'capstone', url: 'https://github.com/aiqbal8520/capstone-project.git'
        }
        }
    }
}