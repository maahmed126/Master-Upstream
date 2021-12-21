pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                build job: 'DevUP' 
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'DownstreamJob'
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'ecs-demo-test'
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'Multistream/main'
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                     }			
        }			
   }		
}
