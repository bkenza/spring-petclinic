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
            }
        }
    }
   post {
    success {
      slackSend (color: '#00FF00', message: "SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]' (${env.BUILD_URL})");
    }
}
