pipeline {
   agent { dockerfile true }

   stages {
      stage('Tests') {
         steps {
            sh '/bin/bash -c "pytest"'
         }
      }
   }

   post {
       always {
           junit testResults: 'latest_test_results.xml', keepLongStdio: true
       }
   }
}