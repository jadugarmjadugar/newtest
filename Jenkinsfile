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
                    docker build -t hello-world .
            
            }
        }
    }   
}
