pipeline{
    agent any
    stages{
        stage("git checkout"){
            steps{
                checkout scm
            }
        }
        stage ("Test"){
            steps{
                sh 'sudo -s apt install npm'
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
