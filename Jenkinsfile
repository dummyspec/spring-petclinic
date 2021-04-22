pipeline{
         agent any
		  tools {
                  maven 'maven-3.8.1'
  }
		 triggers{
                  upstream(upstreamProjects: 'Artifactory_test', threshold: hudson.model.Result.SUCCESS)	
	}
	stages{
	       stage('Source'){
		            steps{
					      git 'https://github.com/dummyrepos/spring-petclinic.git'
					}
		   }
		   stage('package'){
		            steps{
					     sh 'mvn package'
					}
		   }
	}

}
