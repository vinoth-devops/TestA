#!groovy
pipeline{
    agent any
    stages{
        stage('BUILD'){
            steps{
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
