pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def result = build job: 'DownstreamJob', wait: false
                println result.getRawBuild().getLog()
            }			
        }			
    }			
}		

