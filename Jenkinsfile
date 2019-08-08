pipeline {
    agent any
   
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
		
    stage('start release') {

               sh'mvn jgitflow:release-start'
    }


        
    }
}
