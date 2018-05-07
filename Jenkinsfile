pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
		sh 'mvn clean maven-project'
            }
	    post {
	        success {
	    	    echo 'Now Archiving...'
		    archiveArtifacts artifacts: '**/target/*.war'
	        }
	    }
        }
    }
}
