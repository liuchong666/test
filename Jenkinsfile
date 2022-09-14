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
        stage('start') {
            steps {
                echo '启动..'
                 withEnv(['JENKINS_NODE_COOKIE=dontKillMe']) {                
                          sh '''
                            export BUILD_ID=dontKillMe
                            cd /var/lib/jenkins/workspace/newpipeline/WebApplication1/WebApplication1/bin/Release/net6.0/linux-x64/publish/
                            sudo cp -r * /home/liu/test
                            cd /home/liu/test/
                            nohup dotnet WebApplication1.dll --Urls=http://*:7000 &
                            '''                  
                    }
                echo '启动结束'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
