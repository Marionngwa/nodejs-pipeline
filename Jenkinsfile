pipeline {
    agent any 

    tools {
        nodejs 'node2311'
    }

    stages {
        stage('Dependencies & Audit') {
            parallel {
                stage('Install Dependencies') {
                    steps {
                        sh 'npm install --no-audit'
                    }
                }

                stage('NPM Dependency Audit') {
                    steps {
                        sh '''
                            npm audit --audit-level=critical || true
                        '''
                    }
                }
            }
        }
    }
}
