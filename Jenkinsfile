pipeline{
	agent any
	stages{
		stage('Build Application'){
			steps{
				bat 'mvn clean install'
			}
		}


		stage('Deploy Application to Cloudhub'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}

		stage('Perform Regression Testing'){
			steps{
				bat 'newman run F:\\MuleSoft\\Newman\\WorldTimeZone.postman_collection.json --disable-unicode'
			}
		}


	}
}