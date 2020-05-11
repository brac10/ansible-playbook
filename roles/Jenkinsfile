pipeline
{
    agent any

    stages {
        stage('Build Application') {
            steps {
                nodejs("11.9") { sh "npm install" }
            }
        }
        stage('Run Unit Tests') {
            steps {
                nodejs("11.9") { sh "npm test" }
            }
        }
        stage('Deploy Application') {
            steps {
            	nodejs("11.9") { sh "npm start &" }
            }
        }
        stage('Run Functional Tests') {
            steps {
                    nodejs("11.9") { sh "npm run test-wdio" }
                }
            }
        }
}