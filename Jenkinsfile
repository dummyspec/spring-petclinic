pipeline{
         agent any
		 triggers{
                  upstream(upstreamprojects:'Artifactory_test', threshold: hudson.modelResult.SUCCESS)	
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
