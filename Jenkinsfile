pipeline {
    agent {label 'java7'}
    
        stages {
            stage ('clone'){
                step {
                    echo "this is clone stage"
                }
            }
            stage ('Build'){
                tools {
               def MVN_HOME=tool name: 'maven', type: 'maven'
                step {
                    
                    echo "this is Build stage"
                    sh "${MVN_HOME}/bin package"
                }
            }
        }
    }
}
