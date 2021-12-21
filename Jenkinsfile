pipeline {			
    agent any
    triggers {
        upstream(upstreamProjects: 'SuperUpstream',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }
    stages {			
        stage('Build') {			
            steps {			
                build job: 'DevUP' , propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'DownstreamJob', propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'ecs-demo-test', propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'Multistream/main', propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                     }			
        }			
   }		
}
