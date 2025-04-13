pipeline {
    agent any 

    tools {
        nodejs 'node2311'
    }

    stages {
        stage('vm node version'){
            steps {
                sh '''
                    node -v
                    npm -v
                '''
            }
        }
    }
}