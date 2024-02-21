pipeline{
    agent any
    stages{
        stage("git checkout"){
            steps{
                checkout scm
            }
        }
        stage("Prepare") {
            steps {
                sh 'sudo -S apt update && sudo -S apt install -y npm'
            }
        }
        stage ("Test"){
            steps{
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
