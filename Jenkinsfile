pipeline {			
    agent any
    stages {			
        stage {			
            steps {			
                echo 'MASTER UPSTREAM executed'	
            }
            steps {
              build job: 'DownstreamJob', parameters: [
              string(name: 'DownstreamJob', value: env.NAME)
              ], wait: false
}

        }			
    }			
}		

