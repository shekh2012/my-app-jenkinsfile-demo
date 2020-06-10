pipeline{
	agent any
	stages{
		stage('Build Application'){
			steps{
				bat 'mvn clean install'
			}
			
		}
		stage('Deploy Application to CloudHub'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		
		stage('Integration Testing'){
			steps{
				bat 'D:\\node-v12.16.1-win-x64\\newman run D:\\Doctus\\Doctus.postman_collection.json'
			}
		}
		
	}
}
