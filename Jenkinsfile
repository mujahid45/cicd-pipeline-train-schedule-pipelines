 pipeline {
    agent any
	environment {
      DEV = 'Pilot'
      UAT = '2'
      PROD = '3'
      }
      stages {
        stage('test') {
          steps {
            sh 'echo hello'
                }
            }
        stage('test1') {
          steps {
            sh 'echo $TEST'
               }
          }
        stage ('Test 3: Master') {
          when {
            expression {
               DEV == 'Pilot'
            }
           }
          steps { 
             echo 'I only execute on the master branch.' 
                }
              }
        stage ('Test 3: Dev') {
          when { not { branch 'master' } }
              steps {
               echo 'I execute on non-master branches.'
              }
        }       
  }
}
