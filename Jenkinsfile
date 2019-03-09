pipeline {
     environment {
        BRANCH_WORKSPACE = '/var/lib/jenkins/workspace/Train-Test/master/'
    }
    agent {
	node {
	   label 'master'
		customWorkspace "${BRANCH_WORKSPACE}" 
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
