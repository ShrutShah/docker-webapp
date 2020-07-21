node{
    	stage ('SCM Checkout'){
			git credentialsId: 'github', url: 'https://github.com/ShrutShah/docker-webapp.git'
    	}

    	stage('Mvn Package'){
    		def mvnhome = tool name: 'maven-1', type: 'maven'
    		def mvncmd = "($mvnhome)/bin/mvn"
    		sh "($mvncmd) clean package"
    		
    	}

}
	
