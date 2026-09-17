pipeline{
    agent any
  
    stages{
        stage('cloning the repository'){
            steps{
                 git url: 'https://github.com/KaranManhas22/kizaFrontend.git', branch: 'main'

            }
        }
        stage('build'){
            steps{
                sh 'docker build -t kizafrontend .'
            }
        }
        stage('RUN'){
            steps{
                sh 'docker run -d --name frontend-container -p 4200:4200 kizafrontend'
            }
        }
    }
}