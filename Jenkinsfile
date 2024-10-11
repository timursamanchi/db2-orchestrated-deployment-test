#!/usr/bin/env groovy
node {
    // Setting global environment variables at the top
 

    // Enabling timestamps for the build output
    timestamps {
        try {
            stage('Requirements') {
                echo 'Getting Requirements....'
            }

            stage('Build') {
                echo 'Building....'
                echo "the MAX_SIZE = ${MAX_SIZE}"
                echo "the MIN_SIZE = ${MIN_SIZE}"
            }

            stage('Test') {
                // Redefining environment variables specific to the Test stage
                def MAX_SIZE = 9999
                def MIN_SIZE = 9

                echo 'Testing..1'
                echo 'Testing..2'
                echo 'Testing..3'
                echo "the MAX_SIZE = ${MAX_SIZE}"
                echo "the MIN_SIZE = ${MIN_SIZE}"
            }

            stage('Report') {
                echo 'Reporting....'
                sh 'echo "this is a text report generated and archived by a Jenkins pipeline" >> 3stage-report.txt'
                
                archiveArtifacts allowEmptyArchive: true,
                    artifacts: '*.txt',
                    fingerprint: true,
                    followSymlinks: false,
                    onlyIfSuccessful: true
            }

        } catch (Exception e) {
            echo "Pipeline failed: ${e}"
        } finally {
            // Any cleanup actions can go here if needed
        }
    }
}
