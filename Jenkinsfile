pipeline {			
    agent any
    stages {
        stage('TEST') {
            steps {			
                echo 'MASTER UPSTREAM executed'	
            }
        }       
        stage('find-upstream') {
        steps {
        script {
        currentBuild.upstreamBuilds?.each{ b ->
        echo "Triggered by upstream project: ${b.getFullDisplayName()}"
      }  
    }
  } 
}            
}
}
