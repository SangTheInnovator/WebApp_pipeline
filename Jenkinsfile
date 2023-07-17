
pipeline {
    agent any
    
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url:'https://github.com/htrungngx/WebApp_pipeline.git'
            }
        }
        
        stage('Docker build') {
            steps {
                script {
                    docker.withTool('docker') {
                        docker.withRegistry('repo', 'credentials') {
                            sh 'docker build -t dckb9xz/webpipeline:v1 .'
                        }
                    }
                }
            }
        }
    }
}


