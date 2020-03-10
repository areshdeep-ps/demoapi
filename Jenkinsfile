node {
	try {
		stage ('Continuous Integration'){
			env.STAGE = 'Continuous Integration'
			gitCheckoutAll{}
			dir('devops'){
				checkoutUrl(["https://github.com/areshdeep-ps/demoapi.git"], "Master")
			}
			currentBuild.result = "SUCCESS"
		}
		
		stage ('Quality scan') {  
			env.STAGE = 'Quality scan'
			currentBuild.result = "SUCCESS"
        }
	}
	catch(err) {        	
        println "[ERROR]: Build Failed"
		currentBuild.result = "FAILED"
		throw err            
	}
}
