pipeline{
	agent { 
      dockerfile {
         filename 'Dockerfile'
      } 
   }
	stages {
		stage ('index'){
		     steps {
                         sh "cp /go/index.html ${WORKSPACE}"
                         archiveArtifacts "index.html"
                     }
		    
                }
        }
}