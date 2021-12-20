pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
                def checkjob = build job: 'job name', parameters: [ any params here]
                checklog = Jenkins.getInstance().getItemByFullName('job name').getBuildByNumber(checkjob.getNumber()).log
                println checklog
            }			
        }			
    }			
}		
