pipeline{
	agent any 
	stages {
		stage ('Building and runnning image') {
      steps {
        sh 'sudo docker build --tag golang:1 .'
        echo "Building an image"
        sh 'sudo docker run golang:1'
        echo "Running a docker container"
      }
    }
      stage ('index'){
		     steps {
                         sh "cp /go/index.html ${WORKSPACE}"
                         archiveArtifacts "index.html"
                     }
		    
                }
        }
}
             
