pipeline {
    agent {
	    node {
		     label 'master'
		}
	}
    stages {
	    stage('cleaning the workspace') {
		    steps (
			   sh "rm -rf ${WORKSPACE}/*"
			 }
			}
		
		stage('cloaning the Repository') {
		    steps {
			dir ('WORKSPACE'){
			   git url: 'https://github.com/linuxacademy/cicd-pipeline-train-schedule-jenkins.git'
			 }
			}
		}
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}

//pipeline {
//   agent any
//    stages {
//        stage('Build') {
//            steps {
//                echo 'Running build automation'
//                sh './gradlew build --no-daemon'
//                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
//            }
//        }
//    }
//}
