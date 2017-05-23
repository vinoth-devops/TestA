#!groovy
pipeline{
    agent any
    stages{
        stage('BUILD'){
            steps{
                echo "git scm name is " + env.BRANCH_NAME
                checkout scm
                sh '''chmod 677 $WORKSPACE/Test.sh
                sh $WORKSPACE/Test.sh'''
                sh '''echo "I am build guy."
                sleep 10'''                
            }
        }
        stage('DEPLOYMENT'){
            steps{
                 sh '''echo "I am deployment guy."
                sleep 10'''
            }
        }
    }
}
