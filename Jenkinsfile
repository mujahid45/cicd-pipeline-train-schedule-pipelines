pipeline {
    branch_workspace="/var/lib/jenkins/workspace/Train-Test/master/"
    agent {
	    node {
		     label 'master'
			 customWorkspace  ${branch_workspace}
			 
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

