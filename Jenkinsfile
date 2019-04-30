def COMMON_WORKSPACE = '/var/lib/jenkins/workspace/Train-Test/master/'
pipeline {
    agent {
       node {
	  label 'master'
	  customWorkspace "${COMMON_WORKSPACE}"
       }
   }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
		echo 'Hifasdfasd'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
