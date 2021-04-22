pipeline{
         agent any
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
