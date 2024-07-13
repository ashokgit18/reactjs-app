// making changes related to fix JIRA-123
pipeline {
      agent any
      stages {
         stage ('Build') {
          steps {
             sh '''cd $WORKSPACE
                   docker build -t containerstore123:v${BUILD_NUMBER}'''
             }
           }
           stage('push ECR'){
            steps {
                sh '''aws ecr get-login-password --region us-west-2 | docker login --username AWS --password-stdin 637423237872.dkr.ecr.us-west-2.amazonaws.com
           		    
		    docker tag containerstore123:latest 637423237872.dkr.ecr.us-west-2.amazonaws.com/containerstore123:v${BUILD_NUMBER}
		      docker push 637423237872.dkr.ecr.us-west-2.amazonaws.com/containerstore123:v${BUILD_NUMBER}
		   
       '''
            }
          }
          }
        }
