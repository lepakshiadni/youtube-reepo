pipline{
    agent any
    stages{
        stage("git checkout"){
            steps{
                checkout
            }
        }
        stage ("Test"){
            steps{
                sh 'sudo npm install'
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
