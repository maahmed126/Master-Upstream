pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'		
                upstreamBuilds = manager.build.getUpstreamBuilds();
                upstreamJob = upstreamBuilds.keySet().iterator().next();
                lastUpstreamBuild = upstreamJob.getLastBuild();
                if(lastUpstreamBuild.getResult().isBetterThan(manager.build.result)) {
               lastUpstreamBuild.setResult(manager.build.result);
}              
            }			
        }			
   }		
 
