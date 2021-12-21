pipeline {			
    agent any
    triggers {
        upstream(upstreamProjects: 'SuperUpstream',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }
    stages {			
        stage('Build') {			
            steps {			
                build job: 'DevUP' 
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'DownstreamJob'	
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                     }			
        }			
   }		
}
