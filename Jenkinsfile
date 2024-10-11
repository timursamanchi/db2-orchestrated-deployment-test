#!/usr/bin/env groovy
node {
    // Setting global environment variables at the top
 

    // Enabling timestamps for the build output
    timestamps {

        timeout (time: 1, unit: 'HOURS'){ 
            try {
                stage('Requirements') {
                    echo 'Getting Requirements....'
                }

                stage('Build') {
                    echo 'Building....'
  
                }

                stage('Test') {
                    // Redefining environment variables specific to the Test stage

                    echo 'Testing..1'
                    echo 'Testing..2'

                }
            } 
            catch (Exception e) {
                echo "Pipeline failed: ${e}"
                echo "an error occured: ${e.message()}"
            } 
            finally {
            // Any cleanup actions can go here if needed
            }
        }   
    }
}
