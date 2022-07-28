pipeline {
    agent any
    tools {
        nodejs '17.3.1'
    }
    stages{
        stage('Testing stage') {
            steps{
                git url: 'https://github.com/CuongFlodric/aws-mobile-android-notes-tutorial', branch: 'master'
                sh 'node script/upload.js'
            }
        }
    }
}
