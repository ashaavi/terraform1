pipeline {
    agent {
        label ('terraform-slave')
    stages{
        stage ('Git Checkout') {
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/ashaavi/terraform1.git']])
            }
        }
        stage ('terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage ('terraform apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
