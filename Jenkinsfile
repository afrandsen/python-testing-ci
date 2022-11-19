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
           junit testresults: 'latest_test_results.xml', keepLongStdio: true
       }
   }
}