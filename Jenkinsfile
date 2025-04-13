pipeline {
    agent any 

    tools {
        nodejs 'node2311'
    }

    stages {
        stage('installing dependencies'){
            steps {
                sh 'npm install --no-audit'
            }
        }
    }
}