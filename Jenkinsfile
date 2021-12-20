pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def checkjob = build job:'${JOB_NAME}', parameters: [ any params here]
                checklog = Jenkins.getInstance().getItemByFullName('${JOB_NAME}').getBuildByNumber(checkjob.getNumber()).log
                println checklog
            }			
        }			
    }			
}		
