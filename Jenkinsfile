pipeline {
    agent any
    stages {
        stage("git checkout") {
            steps {
                checkout scm
            }
        }
        stage("Test") {
            steps {
                script {
                    // Install npm using sudo
                    sh 'sudo apt install npm'
                    
                    // Run npm test
                    sh 'npm test'
                }
            }
        }
        stage("Build") {
            steps {
                // Run npm build
                sh 'npm run build'
            }
        }
    }
}
