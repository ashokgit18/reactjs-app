// making changes related to fix JIRA-123
pipeline {
      agent any
	options { buildDiscarder(logRotator(numToKeepStr: '2')) }
      stages {
         stage ('Build') {
          steps {
             sh '''cd $WORKSPACE
                   docker build -t containerstore123:v${BUILD_NUMBER} .'''
             }
           }
          // stage('push ECR'){
           // steps {
              // sh '''aws ecr get-login-password --region us-west-2 | docker login --username AWS --password-stdin 637423237872.dkr.ecr.us-west-2.amazonaws.com
           		    
		   // docker tag containerstore123:v${BUILD_NUMBER} 637423237872.dkr.ecr.us-west-2.amazonaws.com/containerstore123:v${BUILD_NUMBER}
		    //  docker push 637423237872.dkr.ecr.us-west-2.amazonaws.com/containerstore123:v${BUILD_NUMBER}
		   
       '''
            }
          }
          }
        }
