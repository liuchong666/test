pipeline{
	agent any
	stages {
		stage("发布"){
			steps{
				sh '''cd WebApplication1/WebApplication1
				dotnet publish -c Release -r  linux-x64  --self-contained true'''
			}
		}
	}

}