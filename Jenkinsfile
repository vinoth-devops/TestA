#!groovy
pipeline{
    agent any
    stages{
        stage('BUILD'){
            steps{
                echo "git env.BRANCH_NAME is " + env.BRANCH_NAME
                echo "git env.CHANGE_ID is " + env.CHANGE_ID
                checkout scm
                sh '''chmod 677 $WORKSPACE/Test.sh
                sh $WORKSPACE/Test.sh'''
                sh '''echo "I am common guy."
                sleep 10'''    
                echo "Added from test123"
            }
        }
        stage('DEPLOYMENT'){
            when{
                expression{ env.CHANGE_ID == null }
            }
            steps{
                 sh '''echo "I am Normal and not a PR guy."
                sleep 2'''
            }
        }
        stage('PULL REQUEST'){
             when{
                expression{ env.CHANGE_ID != null }
            }
            steps{
                 sh '''echo "I am PULL REQUEST guy."
                sleep 2'''
            }
        }
    }
}
