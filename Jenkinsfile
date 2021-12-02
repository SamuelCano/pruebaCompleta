pipeline{
    agent any
    tools {nodejs "nodejs"}
    stages{
        stage('Install'){
            steps {
                sh 'npm install'
            }
        }

        stage('Test'){
            steps {
                sh 'npm run test --progress false --watch false'
            }
        }
        stage('Build'){
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy'){
            steps {
                sh 'mv dist/jenkins/* C:/nginx/html'
            }
        }
    }

}
