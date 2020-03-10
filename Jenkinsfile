node {
	try {
		stage ('Continuous Integration'){
			env.STAGE = 'Continuous Integration'
			// Checkout and get dependencies
			currentBuild.result = "SUCCESS"
		}
		stage ('Build') {  
			env.STAGE = 'Build'
			// Build code
			currentBuild.result = "SUCCESS"
        	}
		stage ('Quality scan') {  
			env.STAGE = 'Quality scan'
			// Run Qulaity scans
			currentBuild.result = "SUCCESS"
        	}
		stage ('Unit Testing') {  
			env.STAGE = 'Unit Testing'
			// Execute UT's
			currentBuild.result = "SUCCESS"
        	}
		stage ('Docker Build and Push') {  
			env.STAGE = 'Deploy'
			// Build docker 
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
