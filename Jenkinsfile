pipeline{
    agent any
    stages{
        stage("Code"){
            steps{
                git url: 'https://github.com/Gitguru01/node-todo-cicd.git', branch: 'master'
            }
        }
        stage("Build"){
            steps{
                sh 'docker build . -t jenkins-pipeln-image'
            }
        }
        stage("Test"){
            steps{
                echo "Test the Code"
            }
        }
        stage("Deploying"){
            steps{
                sh 'docker-compose down && docker-compose up -d'
            }
        }
    }
}
