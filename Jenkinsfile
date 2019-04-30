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
                echo 'Running buinbnvcnbld automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}

