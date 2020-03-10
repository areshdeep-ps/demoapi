node {
	try {
		stage ('Continuous Integration'){
			env.STAGE = 'Continuous Integration'
			dir('devops'){
				//checkoutUrl(["https://github.com/areshdeep-ps/demoapi.git"], "Master")
			}
			currentBuild.result = "SUCCESS"
		}
		stage ('Build') {  
			env.STAGE = 'Build'
			currentBuild.result = "SUCCESS"
        	}
		stage ('Quality scan') {  
			env.STAGE = 'Quality scan'
			currentBuild.result = "SUCCESS"
        	}
		stage ('Unit Testing') {  
			env.STAGE = 'Unit Testing'
			currentBuild.result = "SUCCESS"
        	}
		stage ('Deploy') {  
			env.STAGE = 'Deploy'
			currentBuild.result = "SUCCESS"
        	}
	}
	catch(err) {        	
        println "[ERROR]: Build Failed"
		currentBuild.result = "FAILED"
		throw err            
	}
}
