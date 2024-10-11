#!/usr/bin/env groovy
node {
    // Setting global environment variables at the top

    properties ([
        parameters ([
            choice ( name: 'TARGET_HOST',
                choices: ['my-hostname-10','my-hostname-20','my-hostname-30','my-hostname-40'],
                description: 'select a target hostname')
        ])
    ])

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
