#!/usr/bin/env groovy

node {
    // configure Jenkins options
    timestamps {

        // cause the script to timeout after 1 hour
        timeout( time: 1, unit: 'HOURS')

        // define the build stages
        try {

            stage ('initialize'){

                echo "initialize db2 build"
            }
        }
        catch (Exception e) {
            
            // handle any errors that occur in the pipeline
            echo "an error occured: ${e.message()}"
            throw e
        }    
    }
}