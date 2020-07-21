node{
    	stage ('SCM Checkout'){
		      git credentialsId: 'github', url: 'https://github.com/ShrutShah/docker-webapp.git'
    	}

    	stage('Mvn clean'){
    		  def mvnhome = tool name: 'maven-1', type: 'maven'
		      def mvncmd = "${mvnhome}/bin/mvn"
		      sh "${mvncmd} clean "
    		
    	}
	stage('Mvn validate'){
    		  def mvnhome = tool name: 'maven-1', type: 'maven'
		      def mvncmd = "${mvnhome}/bin/mvn"
		      sh "${mvncmd} validate"
    		
    	}
	stage('Mvn Compile'){
    		  def mvnhome = tool name: 'maven-1', type: 'maven'
		      def mvncmd = "${mvnhome}/bin/mvn"
		      sh "${mvncmd} compile"
    		
    	}
	stage('Mvn Package'){
    		  def mvnhome = tool name: 'maven-1', type: 'maven'
		      def mvncmd = "${mvnhome}/bin/mvn"
		      sh "${mvncmd} package"
    		
    	}
    stage('Build Docker image'){
              sh 'docker build -t shrutshah/mywebapp:v1 .'

        }




}
