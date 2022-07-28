pipeline {
    agent any
    tools {
        nodejs '17.3.1'
    }

    stages{
        stage('Input Stage') {
            steps {
                script {
                    print("Type of deployment: ${env.ACCESS_KEY}")
                    print("Version number: ${env.SECRET_KEY}")
                }
            }
        }
        stage('Testing stage') {
            steps{
                git url: 'https://github.com/hoangchuahe/aws-mobile-android-notes-tutorial', branch: 'master'
                sh 'node script/upload.js'
            }
        }
    }
}
