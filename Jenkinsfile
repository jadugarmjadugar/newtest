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
                   sh ' docker build -t hello-world .'
                 }
            }
        }
    }   
}
