pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Terraform Init') {
            steps {
                sh 'cd /tf_demo && terraform init'
            }
        }
        stage('Terraform Apply') {
            steps {
                sh 'cd /tf_demo && terraform apply -auto-approve'
            }
        }
    }
}
