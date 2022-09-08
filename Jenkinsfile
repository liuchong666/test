pipeline{
	agent any
	stages {
		stage("git pull"){
			steps{
				git branch: 'main', credentialsId: '514c7629-31cf-45f5-a012-dfb4110f54ae', url: 'https://github.com/liuchong666/test.git'
			}
		}
	}

}