def COMMON_WORKSPACE = '/var/lib/jenkins/workspace/Train-Test/example-solution/'
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
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
