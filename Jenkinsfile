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
                         sh 'sudo docker exec -it golang:1 /bin/bash'
                         sh "cat /go/index.html"
                         archiveArtifacts "index.html"
                     }
		    
                }
        }
}
             
