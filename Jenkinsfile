pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def upstream = currentBuild.rawBuild.getCause(hudson.model.Cause$UpstreamCause)
                echo upstream?.shortDescription

            }			
        }			
    }			
}		
