#!/usr/bin/groovy
library identifier: 'PsObaiLib', changelog: false
node {
	try {
		stage ('Continuous Integration'){
			env.STAGE = 'Continuous Integration'
			cleanWs()
			gitCheckoutAll{}
			dir('devops'){
				//checkoutUrl(["https://del.tools.publicis.sapient.com/bitbucket/scm/morgan/p.s.obai.devops.git"], "Master")
			}
			currentBuild.result = "SUCCESS"
		}
		
		stage ('Quality scan') {  
			env.STAGE = 'Quality scan'
			currentBuild.result = "SUCCESS"
			hipChat(currentBuild.result, env.STAGE)
        }
	}
	catch(err) {        	
        println "[ERROR]: Build Failed"
		currentBuild.result = "FAILED"
		throw err            
	}
}
