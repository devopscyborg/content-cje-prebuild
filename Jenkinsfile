pipeline{
	agent any 
	stages {
		stage ('index'){
		     steps {
                         sh "cp /go/index.html ${WORKSPACE}"
                         archiveArtifacts "index.html"
                     }
		    
                }
        }
}
             
