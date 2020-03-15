// Create PR or whatever
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'I am at the building stage'
                sh './mvnw package' 
            }
        }
        stage('Test'){
            steps {
                echo 'I am at the testing stage'
                sh './mvnw test'
            }
        }
        stage('Package'){
            steps{
                echo 'I am at the packaging stage'
                sh './mvnw package'
            } 
        }
        stage('Deploy'){
            steps{
                echo 'I am at the deployment stage'
                sh 'git push -u origin master'
            }
        }
    }
}
