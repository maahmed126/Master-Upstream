pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def result = build job: 'job_name', wait: true
                println result.getRawBuild().getLog()
            }			
        }			
    }			
}		
