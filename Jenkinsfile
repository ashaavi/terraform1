pipeline {
agent any
    stages{
        stage ('Git Checkout') {
            steps{
                checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Keerthan25/Terraform.git']])
            }
        }
        stage ('terraform init') {
            steps {
                sh 'terraform init'
            }
        }
        stage ('terraform apply') {
            steps {
                sh 'terraform destroy --auto-approve'
            }
        }
    }
}
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
