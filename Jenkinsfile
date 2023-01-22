pipeline {
    agent any
    stages {
        stage("start") {
            steps {
                script {
                    echo "hello"
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    sh 'aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 831202177837.dkr.ecr.us-east-1.amazonaws.com'
                    sh ' docker build -t test .'
                 }
            }
        }
        stage("push") {
            steps {
                script {
                    sh 'docker tag test:latest 831202177837.dkr.ecr.us-east-1.amazonaws.com/test:latest'
                    sh 'docker push 831202177837.dkr.ecr.us-east-1.amazonaws.com/test:latest'
                 }
            }
        }
    }   
}
