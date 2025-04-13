pipeline {
    agent any 

    tools {
        nodejs 'node2311'
    }

    stages {
        parallel {
        stage('installing dependencies'){
            steps {
                sh 'npm install --no-audit'
            }
        }
        stage(' npm dependency audit '){
            steps {
                sh '''
                    npm audit --audit-level=critical
                    echo $?
                '''
            }
        }
        }
    }
}