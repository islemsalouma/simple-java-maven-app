pipeline {
    agent any
   
    stages {
	
	     stage("Delete Workspace"){
            steps {                 
                cleanWs deleteDirs: true
				checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
		
    stage('start release') {
             steps {
               sh'mvn -X jgitflow:release-start'
			 }
    }


        
    }
}
