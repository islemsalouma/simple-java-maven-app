pipeline {
    agent any
   
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
		
    stage('start release') {
             steps {
               sh'mvn jgitflow:release-start'
			 }
    }


        
    }
}
