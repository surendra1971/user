@Library('roboshop-shared-library')_

pipeline {
    agent { label 'WS'}
    stages {                                 // Start of the stages
        stage('Lint Checks') {
            steps {
                script{
                    sample.info('USER')
                }
                sh "echo Installing JSLint"
                sh "npm i jslint"
                sh "node_modules/jslint/bin/jslint.js server.js || true"
            }
        }
        stage('code compile'){
            steps{
                sh 'npm install'
            }
        }
    }                                        // End of the stages
}