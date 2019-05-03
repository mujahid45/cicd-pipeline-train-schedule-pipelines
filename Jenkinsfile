 pipeline {
    agent any
	environment {
      DEV = 'Pilot'
      UAT = '2'
      PROD = '3'
      }
      stages {
        stage ('Test 3: Master') {
			steps {
			    script {
                    if (DEV == 'Pilot') {
                        echo 'I only execute on the Pilot branch'
                    } else {
                        echo 'I execute elsewhere'
                    }
                }
            }
        }
    }
}
