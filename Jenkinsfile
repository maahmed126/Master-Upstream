pipeline {			
    agent any
    def handle = triggerRemoteJob blockBuildUntilComplete: false,
    def status = handle.updateBuildStatusBlocking()
    stages {			
        stage('Build') {			
            steps {			
                build job: 'DevUP' 
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'DownstreamJob'
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'ecs-demo-test' , propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'Multistream/main'
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                     }			
        }			
   }		
}
