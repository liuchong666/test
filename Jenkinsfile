pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '开始构建..'
                sh '''cd WebApplication1
                    cd WebApplication1
                    dotnet publish -c Release -r  linux-x64  --self-contained true'''
                echo '构建结束'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
