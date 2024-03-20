pipeline {
    agent any
    
    stages{
        stage('Code'){
            steps{
                git url: 'https://github.com/Pavizhamleenmary/node-todo-cicd.git', branch: 'master' 
            }
        }
        stage('Build and Test'){
            steps{
                sh 'docker build . -t Pavizhamleenmary/node-todo-test:latest'
            }
        }
        
        stage('Deploy'){
            steps{
                echo "Selected choice: ${params.DeploymentTypet }"
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
