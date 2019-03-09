pipeline {
    agent {
	    node {
		     label 'master'
			 customWorkspace '/var/lib/jenkins/workspace/Train-Test/master/'
			 
		}
	}
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
