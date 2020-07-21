node{
    	stage ('SCM Checkout'){
			git credentialsId: 'github', url: 'https://github.com/ShrutShah/docker-webapp.git'
    	}

    	stage('Mvn Package'){
    		def mvnhome = tool name: 'maven-1', type: 'maven'
    		def mvnCMD = "$(mvnhome)/bin/mvn"
    		sh "$(mvnCMD) clean package"
    		
    	}

}
	
