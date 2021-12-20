pipeline {			
    agent any
    stages {			
        stage('Build') {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
            }
            steps {
              build job: 'DownstreamJob', parameters: [
              string(name: 'upsteam_project_name', value: env.NAME)
              ], wait: false
}

        }			
    }			
}		

