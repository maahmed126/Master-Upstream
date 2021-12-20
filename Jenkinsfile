pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def checkjob = ${JOB_NAME}
                checklog = Jenkins.getInstance().getItemByFullName(${JOB_NAME}).getBuildByNumber(checkjob.getNumber()).log
                println checklog
            }			
        }			
    }			
}		
