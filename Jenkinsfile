pipeline{
    agent any
    tools {
        terraform 'terraform-14'
    }
    stages{
        stage('Git chekout'){
            steps{
                git branch: 'main', credentialsId: '7c171059-0b25-4075-aa2d-6fb95aa7d1d5', url: 'https://github.com/Priyanka-Cloud-Infinite/Jenkins-terraform-s3'
            }
        }
        stage('Terraform init'){
            steps{
                sh 'terraform init'
            }
        }
        stage('Terraform Applying'){
            steps{
                sh 'terraform apply --auto-approve'
            }
        }
    }
}
