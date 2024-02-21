pipeline{
    agent any
    stages{
        stage("git checkout"){
            steps{
                checkout
            }
        }
        stage ("Test"){
            steps{
                sh 'sudo apt install npm'
                sh 'npm test'
            }
        }
        stage("Build"){
            steps{
                sh 'npm run build'
            }
        }
    }
}  
